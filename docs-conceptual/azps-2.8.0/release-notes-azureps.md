---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 83e6039153bcc2b8ccb7ceddfa91609f0d6c7b3f
ms.sourcegitcommit: b4ee3fbaaa2a329ea28308bd1902ae83a34db698
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2019
ms.locfileid: "72380194"
---
## <a name="280---october-2019"></a><span data-ttu-id="71948-103">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="71948-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="71948-104">Genel</span><span class="sxs-lookup"><span data-stu-id="71948-104">General</span></span>
* <span data-ttu-id="71948-105">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="71948-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71948-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-106">Az.Accounts</span></span>
* <span data-ttu-id="71948-107">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71948-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71948-108">Az.ApiManagement</span></span>
* <span data-ttu-id="71948-109">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="71948-110">https://github.com/Azure/azure-powershell/issues/10068 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-111">Az.Automation</span></span>
* <span data-ttu-id="71948-112">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="71948-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71948-113">Az.Batch</span></span>
* <span data-ttu-id="71948-114">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="71948-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-115">Az.Compute</span></span>
* <span data-ttu-id="71948-116">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="71948-117">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="71948-118">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="71948-119">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-120">Az.DataFactory</span></span>
* <span data-ttu-id="71948-121">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="71948-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="71948-122">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="71948-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="71948-123">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-125">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71948-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71948-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="71948-127">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="71948-128">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="71948-129">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="71948-130">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71948-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71948-131">Az.IotHub</span></span>
* <span data-ttu-id="71948-132">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="71948-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="71948-133">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="71948-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="71948-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-134">Az.Monitor</span></span>
* <span data-ttu-id="71948-135">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-135">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="71948-136">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="71948-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="71948-137">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="71948-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="71948-138">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="71948-138">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-139">Az.Network</span></span>
* <span data-ttu-id="71948-140">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="71948-141">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="71948-142">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="71948-142">New cmdlets added:</span></span>
        - <span data-ttu-id="71948-143">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-143">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="71948-144">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="71948-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="71948-145">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="71948-146">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="71948-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="71948-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71948-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71948-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71948-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71948-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71948-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="71948-150">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="71948-151">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="71948-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="71948-152">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="71948-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="71948-153">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="71948-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71948-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71948-154">Az.RedisCache</span></span>
* <span data-ttu-id="71948-155">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-156">Az.Sql</span></span>
* <span data-ttu-id="71948-157">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-158">Az.Storage</span></span>
* <span data-ttu-id="71948-159">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="71948-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="71948-160">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="71948-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="71948-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="71948-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="71948-162">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="71948-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="71948-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71948-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71948-164">Az.StorageSync</span></span>
* <span data-ttu-id="71948-165">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-166">Az.Websites</span></span>
* <span data-ttu-id="71948-167">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="71948-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="71948-168">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="71948-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="71948-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71948-169">Az.ApiManagement</span></span>
* <span data-ttu-id="71948-170">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="71948-171">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="71948-172">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="71948-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-173">Az.Automation</span></span>
* <span data-ttu-id="71948-174">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="71948-175">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="71948-176">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-177">Az.Compute</span></span>
* <span data-ttu-id="71948-178">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="71948-179">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71948-180">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="71948-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="71948-181">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="71948-182">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="71948-183">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="71948-184">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="71948-185">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="71948-186">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-187">Az.DataFactory</span></span>
* <span data-ttu-id="71948-188">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="71948-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="71948-189">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71948-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71948-190">Az.HDInsight</span></span>
* <span data-ttu-id="71948-191">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="71948-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71948-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71948-192">Az.IotHub</span></span>
* <span data-ttu-id="71948-193">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="71948-194">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="71948-195">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="71948-195">New cmdlets are:</span></span>
    - <span data-ttu-id="71948-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71948-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71948-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71948-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71948-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71948-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71948-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="71948-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71948-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-200">Az.Monitor</span></span>
* <span data-ttu-id="71948-201">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="71948-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="71948-202">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="71948-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="71948-203">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="71948-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="71948-204">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="71948-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="71948-205">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="71948-206">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="71948-207">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="71948-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="71948-208">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="71948-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="71948-209">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="71948-210">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="71948-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="71948-211">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="71948-212">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="71948-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="71948-213">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="71948-214">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="71948-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="71948-215">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="71948-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="71948-216">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="71948-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="71948-217">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="71948-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="71948-218">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="71948-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="71948-219">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="71948-220">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-220">Overall improved help files</span></span>
* <span data-ttu-id="71948-221">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-222">Az.Network</span></span>
* <span data-ttu-id="71948-223">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="71948-224">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="71948-225">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="71948-226">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="71948-227">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="71948-228">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="71948-229">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="71948-230">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="71948-231">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="71948-232">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="71948-233">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="71948-234">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="71948-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="71948-235">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-235">New cmdlets</span></span>
        - <span data-ttu-id="71948-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="71948-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="71948-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="71948-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="71948-238">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="71948-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="71948-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="71948-239">New-VpnSite</span></span>
        - <span data-ttu-id="71948-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="71948-240">Update-VpnSite</span></span>
        - <span data-ttu-id="71948-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="71948-241">New-VpnConnection</span></span>
        - <span data-ttu-id="71948-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="71948-242">Update-VpnConnection</span></span>
* <span data-ttu-id="71948-243">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-245">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="71948-246">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-247">Az.Resources</span></span>
* <span data-ttu-id="71948-248">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71948-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="71948-250">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="71948-251">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="71948-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="71948-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71948-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71948-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71948-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71948-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71948-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71948-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="71948-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="71948-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71948-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71948-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71948-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71948-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71948-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71948-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71948-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71948-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="71948-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="71948-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="71948-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71948-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="71948-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71948-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="71948-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71948-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="71948-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="71948-265">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71948-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71948-266">Az.SignalR</span></span>
* <span data-ttu-id="71948-267">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-268">Az.Sql</span></span>
* <span data-ttu-id="71948-269">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="71948-270">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="71948-271">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="71948-272">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="71948-273">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-274">Az.Storage</span></span>
* <span data-ttu-id="71948-275">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="71948-276">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="71948-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71948-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="71948-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71948-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="71948-279">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="71948-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71948-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="71948-281">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="71948-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71948-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71948-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71948-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71948-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71948-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71948-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="71948-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-286">Az.Websites</span></span>
* <span data-ttu-id="71948-287">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="71948-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="71948-288">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="71948-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="71948-289">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="71948-290">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="71948-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="71948-291">Genel</span><span class="sxs-lookup"><span data-stu-id="71948-291">General</span></span>
* <span data-ttu-id="71948-292">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71948-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-293">Az.Accounts</span></span>
* <span data-ttu-id="71948-294">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="71948-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="71948-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71948-295">Az.Aks</span></span>
* <span data-ttu-id="71948-296">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="71948-297">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="71948-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71948-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71948-298">Az.ApiManagement</span></span>
* <span data-ttu-id="71948-299">https://github.com/Azure/azure-powershell/issues/9351 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="71948-300">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="71948-301">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="71948-302">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="71948-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="71948-303">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71948-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71948-304">Az.Batch</span></span>
* <span data-ttu-id="71948-305">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71948-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71948-306">Az.Cdn</span></span>
* <span data-ttu-id="71948-307">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-308">Az.Compute</span></span>
* <span data-ttu-id="71948-309">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="71948-310">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="71948-311">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="71948-312">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="71948-313">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="71948-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="71948-314">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="71948-315">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="71948-316">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-317">Az.DataFactory</span></span>
* <span data-ttu-id="71948-318">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="71948-319">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="71948-320">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="71948-321">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-323">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71948-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71948-324">Az.EventHub</span></span>
* <span data-ttu-id="71948-325">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="71948-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="71948-326">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="71948-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="71948-327">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="71948-328">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="71948-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="71948-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="71948-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="71948-330">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71948-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-331">Az.Monitor</span></span>
* <span data-ttu-id="71948-332">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-333">Az.Network</span></span>
* <span data-ttu-id="71948-334">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="71948-335">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="71948-336">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="71948-337">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="71948-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="71948-338">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="71948-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="71948-339">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="71948-340">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71948-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71948-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="71948-342">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="71948-343">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-343">Added example</span></span>
    - <span data-ttu-id="71948-344">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="71948-345">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="71948-346">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-348">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-349">Az.Resources</span></span>
* <span data-ttu-id="71948-350">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="71948-351">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="71948-352">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="71948-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="71948-353">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71948-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71948-354">Az.ServiceBus</span></span>
* <span data-ttu-id="71948-355">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="71948-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="71948-356">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="71948-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="71948-357">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="71948-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="71948-359">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="71948-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="71948-360">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="71948-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="71948-361">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="71948-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="71948-362">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="71948-363">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="71948-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="71948-364">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-365">Az.Sql</span></span>
* <span data-ttu-id="71948-366">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-367">Az.Storage</span></span>
* <span data-ttu-id="71948-368">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="71948-369">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="71948-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="71948-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71948-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="71948-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71948-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="71948-372">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="71948-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="71948-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71948-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-374">Az.Websites</span></span>
* <span data-ttu-id="71948-375">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="71948-376">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="71948-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-377">Az.Accounts</span></span>
* <span data-ttu-id="71948-378">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="71948-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="71948-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="71948-380">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="71948-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-381">Az.Automation</span></span>
* <span data-ttu-id="71948-382">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="71948-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71948-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="71948-384">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-385">Az.Compute</span></span>
* <span data-ttu-id="71948-386">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="71948-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71948-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71948-388">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="71948-389">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="71948-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-390">Az.DataFactory</span></span>
* <span data-ttu-id="71948-391">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="71948-392">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71948-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71948-393">Az.EventHub</span></span>
* <span data-ttu-id="71948-394">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="71948-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="71948-395">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71948-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71948-396">Az.KeyVault</span></span>
* <span data-ttu-id="71948-397">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71948-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71948-398">Az.LogicApp</span></span>
* <span data-ttu-id="71948-399">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="71948-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="71948-400">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="71948-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="71948-401">Az.ManagedServices</span></span>
* <span data-ttu-id="71948-402">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="71948-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-403">Az.Network</span></span>
* <span data-ttu-id="71948-404">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="71948-405">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-405">New cmdlets</span></span>
        - <span data-ttu-id="71948-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71948-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71948-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71948-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71948-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71948-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71948-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71948-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71948-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71948-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71948-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71948-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71948-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="71948-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="71948-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71948-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="71948-414">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="71948-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="71948-415">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="71948-416">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="71948-417">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="71948-418">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="71948-419">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="71948-420">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-420">Updated cmdlets</span></span>
        - <span data-ttu-id="71948-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71948-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71948-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71948-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71948-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71948-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="71948-424">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="71948-425">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="71948-426">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="71948-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="71948-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="71948-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="71948-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="71948-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="71948-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="71948-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="71948-430">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="71948-431">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="71948-432">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="71948-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71948-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71948-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="71948-434">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="71948-435">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-437">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="71948-438">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="71948-439">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="71948-440">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="71948-441">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="71948-442">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="71948-443">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="71948-444">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="71948-445">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="71948-446">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-447">Az.Resources</span></span>
- <span data-ttu-id="71948-448">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="71948-449">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71948-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71948-450">Az.ServiceBus</span></span>
* <span data-ttu-id="71948-451">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="71948-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="71948-452">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-453">Az.Sql</span></span>
* <span data-ttu-id="71948-454">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="71948-455">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="71948-456">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-457">Az.Storage</span></span>
* <span data-ttu-id="71948-458">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71948-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71948-459">Az.StorageSync</span></span>
* <span data-ttu-id="71948-460">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="71948-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="71948-461">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-462">Az.Websites</span></span>
* <span data-ttu-id="71948-463">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="71948-464">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="71948-465">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="71948-466">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="71948-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-467">Az.Accounts</span></span>
* <span data-ttu-id="71948-468">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="71948-469">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="71948-470">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="71948-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="71948-471">Az.Advisor</span></span>
* <span data-ttu-id="71948-472">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="71948-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="71948-473">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="71948-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71948-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71948-474">Az.ApiManagement</span></span>
* <span data-ttu-id="71948-475">https://github.com/Azure/azure-powershell/issues/8671 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="71948-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="71948-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="71948-477">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="71948-478">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="71948-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="71948-479">https://github.com/Azure/azure-powershell/issues/9307 ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="71948-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="71948-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="71948-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="71948-481">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-482">Az.Automation</span></span>
* <span data-ttu-id="71948-483">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-484">Az.Compute</span></span>
* <span data-ttu-id="71948-485">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-486">Az.DataFactory</span></span>
* <span data-ttu-id="71948-487">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="71948-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71948-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71948-488">Az.EventGrid</span></span>
* <span data-ttu-id="71948-489">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71948-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71948-490">Az.IotHub</span></span>
* <span data-ttu-id="71948-491">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-492">Az.Network</span></span>
* <span data-ttu-id="71948-493">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="71948-494">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71948-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71948-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="71948-496">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="71948-497">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="71948-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71948-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71948-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="71948-499">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-501">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="71948-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-502">Az.Resources</span></span>
    - <span data-ttu-id="71948-503">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="71948-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="71948-504">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="71948-505">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="71948-506">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71948-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71948-507">Az.ServiceBus</span></span>
* <span data-ttu-id="71948-508">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-509">Az.Sql</span></span>
* <span data-ttu-id="71948-510">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="71948-511">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="71948-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="71948-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71948-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71948-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71948-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71948-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71948-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71948-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71948-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="71948-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71948-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="71948-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71948-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="71948-518">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-519">Az.Storage</span></span>
* <span data-ttu-id="71948-520">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="71948-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="71948-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71948-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="71948-522">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="71948-523">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="71948-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="71948-524">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="71948-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="71948-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="71948-527">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="71948-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71948-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="71948-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71948-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71948-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71948-530">Az.StorageSync</span></span>
* <span data-ttu-id="71948-531">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="71948-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="71948-532">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="71948-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-533">Az.Accounts</span></span>
* <span data-ttu-id="71948-534">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="71948-535">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="71948-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="71948-536">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="71948-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="71948-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="71948-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="71948-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-539">Az.Compute</span></span>
* <span data-ttu-id="71948-540">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="71948-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="71948-541">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="71948-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="71948-542">Az.Dns</span></span>
* <span data-ttu-id="71948-543">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71948-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71948-544">Az.EventGrid</span></span>
* <span data-ttu-id="71948-545">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="71948-546">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="71948-546">New cmdlets:</span></span>
    - <span data-ttu-id="71948-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71948-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71948-548">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71948-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71948-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71948-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71948-550">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="71948-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="71948-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71948-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71948-552">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71948-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71948-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="71948-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="71948-554">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="71948-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71948-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="71948-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="71948-556">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="71948-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="71948-557">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="71948-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="71948-558">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71948-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="71948-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="71948-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="71948-560">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="71948-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="71948-561">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="71948-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="71948-562">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71948-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="71948-563">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="71948-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="71948-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="71948-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="71948-565">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="71948-566">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="71948-567">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="71948-568">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="71948-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="71948-569">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="71948-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="71948-570">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="71948-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="71948-571">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="71948-572">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="71948-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="71948-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="71948-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="71948-574">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="71948-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="71948-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="71948-576">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="71948-577">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71948-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71948-578">Az.FrontDoor</span></span>
* <span data-ttu-id="71948-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="71948-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="71948-580">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="71948-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="71948-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="71948-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="71948-582">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="71948-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-583">Az.Network</span></span>
* <span data-ttu-id="71948-584">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="71948-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="71948-585">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-585">New cmdlets</span></span>
        - <span data-ttu-id="71948-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="71948-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="71948-587">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="71948-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="71948-588">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-588">New cmdlets</span></span> 
        - <span data-ttu-id="71948-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="71948-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="71948-590">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="71948-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="71948-591">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-591">New cmdlets</span></span> 
        - <span data-ttu-id="71948-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71948-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="71948-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71948-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71948-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71948-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71948-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="71948-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="71948-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71948-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="71948-597">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="71948-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="71948-598">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-598">New cmdlets</span></span>
        - <span data-ttu-id="71948-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71948-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71948-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71948-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71948-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71948-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71948-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="71948-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="71948-603">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="71948-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="71948-604">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="71948-605">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="71948-606">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="71948-607">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="71948-608">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="71948-609">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="71948-610">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="71948-611">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="71948-612">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="71948-613">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="71948-614">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="71948-615">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="71948-616">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="71948-617">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="71948-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="71948-618">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="71948-619">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="71948-620">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="71948-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="71948-621">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="71948-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="71948-622">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="71948-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="71948-623">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="71948-624">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="71948-625">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71948-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71948-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="71948-627">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-628">Az.Resources</span></span>
* <span data-ttu-id="71948-629">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="71948-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="71948-630">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="71948-631">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="71948-632">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71948-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="71948-634">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-635">Az.Sql</span></span>
* <span data-ttu-id="71948-636">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="71948-637">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="71948-638">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="71948-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71948-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71948-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71948-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71948-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71948-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71948-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="71948-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="71948-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="71948-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-644">Az.Storage</span></span>
* <span data-ttu-id="71948-645">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="71948-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="71948-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="71948-647">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="71948-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-649">Az.Websites</span></span>
* <span data-ttu-id="71948-650">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="71948-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="71948-651">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="71948-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="71948-652">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="71948-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="71948-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71948-653">Az.Cdn</span></span>
* <span data-ttu-id="71948-654">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-655">Az.Compute</span></span>
* <span data-ttu-id="71948-656">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="71948-657">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="71948-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71948-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71948-658">Az.EventHub</span></span>
* <span data-ttu-id="71948-659">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="71948-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="71948-660">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="71948-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-661">Az.Network</span></span>
* <span data-ttu-id="71948-662">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="71948-663">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71948-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71948-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="71948-665">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-667">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71948-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71948-668">Az.ServiceBus</span></span>
* <span data-ttu-id="71948-669">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="71948-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71948-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="71948-671">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="71948-672">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-673">Az.Sql</span></span>
* <span data-ttu-id="71948-674">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="71948-675">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="71948-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="71948-676">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="71948-677">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="71948-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-678">Az.Websites</span></span>
* <span data-ttu-id="71948-679">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="71948-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="71948-680">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="71948-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="71948-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71948-681">Az.ApiManagement</span></span>
* <span data-ttu-id="71948-682">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="71948-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="71948-683">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="71948-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="71948-684">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="71948-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="71948-685">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="71948-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="71948-686">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71948-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="71948-687">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="71948-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="71948-688">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="71948-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="71948-689">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="71948-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="71948-690">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="71948-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="71948-691">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="71948-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="71948-692">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="71948-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="71948-693">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="71948-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="71948-694">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="71948-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="71948-695">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="71948-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="71948-696">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="71948-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="71948-697">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="71948-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="71948-698">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="71948-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="71948-699">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="71948-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="71948-700">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="71948-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="71948-701">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="71948-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="71948-702">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="71948-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="71948-703">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="71948-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="71948-704">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="71948-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="71948-705">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="71948-706">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="71948-707">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="71948-708">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="71948-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="71948-709">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="71948-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="71948-710">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="71948-711">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="71948-712">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="71948-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="71948-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="71948-714">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="71948-715">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="71948-716">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="71948-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="71948-717">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="71948-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="71948-718">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="71948-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="71948-719">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="71948-720">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="71948-721">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="71948-722">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="71948-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="71948-723">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="71948-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="71948-724">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="71948-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="71948-725">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="71948-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="71948-726">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="71948-727">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="71948-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="71948-728">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="71948-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="71948-729">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="71948-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="71948-730">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="71948-731">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="71948-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="71948-732">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="71948-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="71948-733">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="71948-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="71948-734">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="71948-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="71948-735">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="71948-736">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="71948-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="71948-737">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="71948-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="71948-738">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="71948-739">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="71948-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="71948-740">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="71948-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="71948-741">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="71948-742">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="71948-743">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="71948-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="71948-744">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="71948-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="71948-745">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="71948-746">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="71948-747">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="71948-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="71948-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="71948-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="71948-749">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="71948-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="71948-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="71948-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="71948-751">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="71948-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="71948-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="71948-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="71948-753">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="71948-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="71948-754">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="71948-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="71948-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="71948-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="71948-756">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="71948-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="71948-757">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="71948-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="71948-758">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="71948-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-759">Az.Automation</span></span>
* <span data-ttu-id="71948-760">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="71948-761">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="71948-762">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="71948-763">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="71948-764">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="71948-765">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="71948-766">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="71948-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-767">Az.Compute</span></span>
* <span data-ttu-id="71948-768">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="71948-769">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="71948-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-771">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71948-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-772">Az.Monitor</span></span>
* <span data-ttu-id="71948-773">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-774">Az.Network</span></span>
* <span data-ttu-id="71948-775">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="71948-776">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="71948-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="71948-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="71948-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="71948-778">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-779">Az.Resources</span></span>
* <span data-ttu-id="71948-780">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-781">Az.Sql</span></span>
* <span data-ttu-id="71948-782">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="71948-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="71948-783">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="71948-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-784">Az.Accounts</span></span>
* <span data-ttu-id="71948-785">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="71948-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71948-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71948-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="71948-787">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="71948-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="71948-788">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="71948-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-789">Az.Compute</span></span>
* <span data-ttu-id="71948-790">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="71948-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="71948-791">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="71948-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="71948-792">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="71948-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="71948-793">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="71948-794">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="71948-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="71948-795">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="71948-796">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="71948-796">Breaking changes</span></span>
    - <span data-ttu-id="71948-797">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="71948-798">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="71948-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="71948-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="71948-800">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="71948-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="71948-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="71948-801">Az.Dns</span></span>
* <span data-ttu-id="71948-802">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="71948-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="71948-803">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="71948-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="71948-804">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71948-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71948-805">Az.FrontDoor</span></span>
* <span data-ttu-id="71948-806">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="71948-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="71948-807">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="71948-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="71948-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71948-808">Az.HDInsight</span></span>
* <span data-ttu-id="71948-809">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="71948-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="71948-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71948-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="71948-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71948-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="71948-812">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="71948-813">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="71948-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="71948-814">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="71948-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="71948-815">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="71948-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71948-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-816">Az.Monitor</span></span>
* <span data-ttu-id="71948-817">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="71948-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="71948-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="71948-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="71948-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="71948-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="71948-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="71948-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="71948-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="71948-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="71948-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="71948-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="71948-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="71948-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="71948-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71948-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71948-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71948-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71948-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71948-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71948-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71948-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71948-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71948-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71948-829">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="71948-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="71948-830">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-831">Az.Network</span></span>
* <span data-ttu-id="71948-832">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="71948-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="71948-833">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-833">New cmdlets</span></span>
        - <span data-ttu-id="71948-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71948-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="71948-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71948-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="71948-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71948-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="71948-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71948-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="71948-838">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-838">Updated cmdlets</span></span>
        - <span data-ttu-id="71948-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="71948-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="71948-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="71948-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="71948-841">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="71948-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="71948-842">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="71948-843">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71948-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71948-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="71948-845">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="71948-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="71948-846">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="71948-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="71948-847">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="71948-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-849">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="71948-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="71948-850">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="71948-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="71948-851">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="71948-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="71948-852">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="71948-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="71948-853">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="71948-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="71948-854">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="71948-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="71948-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="71948-855">Az.Relay</span></span>
* <span data-ttu-id="71948-856">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="71948-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71948-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71948-857">Az.ServiceBus</span></span>
* <span data-ttu-id="71948-858">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-859">Az.Storage</span></span>
* <span data-ttu-id="71948-860">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="71948-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="71948-861">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="71948-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="71948-862">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="71948-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="71948-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="71948-864">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="71948-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="71948-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="71948-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="71948-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-868">Az.Websites</span></span>
* <span data-ttu-id="71948-869">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="71948-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="71948-870">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="71948-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="71948-871">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="71948-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71948-872">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="71948-872">Highlights since the last major release</span></span>
* <span data-ttu-id="71948-873">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="71948-873">General availability of `Az` module</span></span>
* <span data-ttu-id="71948-874">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71948-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71948-875">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71948-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71948-876">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71948-877">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71948-878">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71948-879">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71948-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-880">Az.Accounts</span></span>
* <span data-ttu-id="71948-881">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71948-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71948-882">Az.Batch</span></span>
* <span data-ttu-id="71948-883">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71948-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71948-884">Az.Cdn</span></span>
* <span data-ttu-id="71948-885">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71948-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71948-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="71948-887">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-888">Az.Compute</span></span>
* <span data-ttu-id="71948-889">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="71948-890">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71948-891">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-892">Az.DataFactory</span></span>
* <span data-ttu-id="71948-893">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-895">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71948-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71948-896">Az.EventGrid</span></span>
* <span data-ttu-id="71948-897">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71948-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71948-898">Az.EventHub</span></span>
* <span data-ttu-id="71948-899">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="71948-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71948-900">Az.HDInsight</span></span>
* <span data-ttu-id="71948-901">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71948-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71948-902">Az.IotHub</span></span>
* <span data-ttu-id="71948-903">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71948-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71948-904">Az.KeyVault</span></span>
* <span data-ttu-id="71948-905">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71948-906">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="71948-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="71948-907">Az.MachineLearning</span></span>
* <span data-ttu-id="71948-908">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="71948-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="71948-909">Az.Media</span></span>
* <span data-ttu-id="71948-910">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71948-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-911">Az.Monitor</span></span>
  * <span data-ttu-id="71948-912">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="71948-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="71948-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="71948-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="71948-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="71948-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="71948-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71948-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="71948-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71948-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="71948-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71948-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="71948-918">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-919">Az.Network</span></span>
* <span data-ttu-id="71948-920">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71948-921">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="71948-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="71948-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="71948-923">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71948-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71948-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="71948-925">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="71948-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="71948-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="71948-927">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-929">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71948-930">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="71948-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="71948-931">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="71948-932">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71948-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71948-933">Az.RedisCache</span></span>
* <span data-ttu-id="71948-934">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-935">Az.Resources</span></span>
* <span data-ttu-id="71948-936">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-937">Az.Sql</span></span>
* <span data-ttu-id="71948-938">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="71948-939">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71948-940">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="71948-941">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="71948-942">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="71948-943">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="71948-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="71948-944">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-945">Az.Websites</span></span>
* <span data-ttu-id="71948-946">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="71948-947">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71948-948">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="71948-949">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="71948-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="71948-950">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="71948-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71948-951">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="71948-951">Highlights since the last major release</span></span>
* <span data-ttu-id="71948-952">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="71948-952">General availability of `Az` module</span></span>
* <span data-ttu-id="71948-953">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71948-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71948-954">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71948-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71948-955">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71948-956">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71948-957">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71948-958">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71948-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-959">Az.Accounts</span></span>
* <span data-ttu-id="71948-960">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71948-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71948-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="71948-962">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="71948-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="71948-963">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="71948-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-964">Az.Automation</span></span>
* <span data-ttu-id="71948-965">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="71948-966">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="71948-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="71948-967">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="71948-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-968">Az.Compute</span></span>
* <span data-ttu-id="71948-969">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71948-970">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="71948-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="71948-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71948-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="71948-972">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-973">Az.DataFactory</span></span>
* <span data-ttu-id="71948-974">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="71948-975">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-976">Az.Resources</span></span>
* <span data-ttu-id="71948-977">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="71948-978">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="71948-979">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="71948-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="71948-980">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="71948-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="71948-981">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="71948-982">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="71948-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-983">Az.Sql</span></span>
* <span data-ttu-id="71948-984">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="71948-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-985">Az.Storage</span></span>
* <span data-ttu-id="71948-986">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="71948-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="71948-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="71948-987">New-AzStorageContext</span></span>
* <span data-ttu-id="71948-988">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="71948-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="71948-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71948-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="71948-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71948-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="71948-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="71948-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="71948-993">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="71948-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="71948-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71948-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="71948-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71948-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="71948-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71948-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="71948-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71948-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="71948-998">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="71948-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71948-999">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="71948-999">Highlights since the last major release</span></span>
* <span data-ttu-id="71948-1000">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="71948-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="71948-1001">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71948-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71948-1002">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71948-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71948-1003">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71948-1004">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71948-1005">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71948-1006">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-1007">Az.Automation</span></span>
* <span data-ttu-id="71948-1008">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="71948-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="71948-1009">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="71948-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="71948-1010">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="71948-1010">Pre-Post script</span></span>
    * <span data-ttu-id="71948-1011">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="71948-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1012">Az.Compute</span></span>
* <span data-ttu-id="71948-1013">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="71948-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="71948-1014">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71948-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71948-1015">Az.KeyVault</span></span>
* <span data-ttu-id="71948-1016">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1017">Az.Network</span></span>
* <span data-ttu-id="71948-1018">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="71948-1019">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-1021">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="71948-1022">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1023">Az.Resources</span></span>
* <span data-ttu-id="71948-1024">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="71948-1025">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1026">Az.Sql</span></span>
* <span data-ttu-id="71948-1027">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-1028">Az.Storage</span></span>
* <span data-ttu-id="71948-1029">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="71948-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="71948-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71948-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71948-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71948-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="71948-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="71948-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="71948-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="71948-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="71948-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-1036">Az.Websites</span></span>
* <span data-ttu-id="71948-1037">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="71948-1038">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="71948-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-1039">Az.Accounts</span></span>
* <span data-ttu-id="71948-1040">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="71948-1041">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-1042">Az.Automation</span></span>
* <span data-ttu-id="71948-1043">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="71948-1044">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="71948-1045">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="71948-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71948-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71948-1046">Az.Cdn</span></span>
* <span data-ttu-id="71948-1047">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="71948-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1048">Az.Compute</span></span>
* <span data-ttu-id="71948-1049">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-1050">Az.DataFactory</span></span>
* <span data-ttu-id="71948-1051">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71948-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71948-1052">Az.LogicApp</span></span>
* <span data-ttu-id="71948-1053">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="71948-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1054">Az.Network</span></span>
* <span data-ttu-id="71948-1055">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-1057">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="71948-1058">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="71948-1058">SDK Update</span></span>
* <span data-ttu-id="71948-1059">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="71948-1060">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1061">Az.Resources</span></span>
* <span data-ttu-id="71948-1062">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="71948-1063">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="71948-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="71948-1064">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="71948-1065">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="71948-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="71948-1066">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="71948-1067">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="71948-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1068">Az.Sql</span></span>
* <span data-ttu-id="71948-1069">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="71948-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="71948-1070">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="71948-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-1071">Az.Storage</span></span>
* <span data-ttu-id="71948-1072">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71948-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="71948-1073">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="71948-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="71948-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71948-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="71948-1075">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="71948-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-1076">Az.Automation</span></span>
* <span data-ttu-id="71948-1077">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="71948-1078">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="71948-1079">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71948-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71948-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="71948-1081">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1082">Az.Compute</span></span>
* <span data-ttu-id="71948-1083">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="71948-1084">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="71948-1085">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="71948-1086">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="71948-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-1088">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71948-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71948-1089">Az.EventHub</span></span>
* <span data-ttu-id="71948-1090">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="71948-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71948-1091">Az.KeyVault</span></span>
* <span data-ttu-id="71948-1092">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71948-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71948-1093">Az.LogicApp</span></span>
* <span data-ttu-id="71948-1094">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="71948-1095">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="71948-1096">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="71948-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71948-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71948-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71948-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71948-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71948-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71948-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="71948-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="71948-1101">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="71948-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="71948-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71948-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71948-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71948-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71948-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71948-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71948-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="71948-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="71948-1106">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71948-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-1107">Az.Monitor</span></span>
* <span data-ttu-id="71948-1108">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1109">Az.Network</span></span>
* <span data-ttu-id="71948-1110">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71948-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71948-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="71948-1112">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="71948-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="71948-1113">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="71948-1114">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="71948-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1115">Az.Resources</span></span>
* <span data-ttu-id="71948-1116">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="71948-1117">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="71948-1118">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="71948-1119">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1120">Az.Sql</span></span>
* <span data-ttu-id="71948-1121">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="71948-1122">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-1123">Az.Websites</span></span>
* <span data-ttu-id="71948-1124">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="71948-1125">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="71948-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-1126">Az.Accounts</span></span>
* <span data-ttu-id="71948-1127">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="71948-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71948-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71948-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="71948-1129">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="71948-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1130">Az.Compute</span></span>
* <span data-ttu-id="71948-1131">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="71948-1132">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="71948-1133">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="71948-1135">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="71948-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1136">Az.Resources</span></span>
* <span data-ttu-id="71948-1137">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="71948-1138">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="71948-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="71948-1139">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="71948-1140">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="71948-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1141">Az.Sql</span></span>
* <span data-ttu-id="71948-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71948-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="71948-1143">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="71948-1144">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="71948-1145">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="71948-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-1146">Az.Accounts</span></span>
* <span data-ttu-id="71948-1147">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="71948-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71948-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71948-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="71948-1149">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="71948-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71948-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="71948-1151">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="71948-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="71948-1152">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="71948-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-1153">Az.Accounts</span></span>
* <span data-ttu-id="71948-1154">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71948-1155">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71948-1156">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="71948-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71948-1157">Az.Aks</span></span>
* <span data-ttu-id="71948-1158">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71948-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-1159">Az.Automation</span></span>
* <span data-ttu-id="71948-1160">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="71948-1161">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71948-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71948-1162">Az.Cdn</span></span>
* <span data-ttu-id="71948-1163">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1164">Az.Compute</span></span>
* <span data-ttu-id="71948-1165">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="71948-1166">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="71948-1167">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="71948-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71948-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71948-1169">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71948-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71948-1170">Az.DataFactory</span></span>
* <span data-ttu-id="71948-1171">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-1173">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="71948-1174">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="71948-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="71948-1175">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71948-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71948-1176">Az.IotHub</span></span>
* <span data-ttu-id="71948-1177">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71948-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71948-1178">Az.KeyVault</span></span>
* <span data-ttu-id="71948-1179">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1180">Az.Network</span></span>
* <span data-ttu-id="71948-1181">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1182">Az.Resources</span></span>
* <span data-ttu-id="71948-1183">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="71948-1184">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="71948-1185">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="71948-1186">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="71948-1187">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="71948-1188">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="71948-1189">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="71948-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71948-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="71948-1191">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="71948-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="71948-1192">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1192">Fix some error messages.</span></span>
* <span data-ttu-id="71948-1193">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="71948-1194">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71948-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71948-1195">Az.SignalR</span></span>
* <span data-ttu-id="71948-1196">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1197">Az.Sql</span></span>
* <span data-ttu-id="71948-1198">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71948-1199">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="71948-1200">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="71948-1201">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="71948-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-1202">Az.Storage</span></span>
* <span data-ttu-id="71948-1203">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71948-1204">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="71948-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="71948-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="71948-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="71948-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="71948-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="71948-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="71948-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="71948-1208">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-1209">Az.Websites</span></span>
* <span data-ttu-id="71948-1210">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71948-1211">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="71948-1212">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="71948-1213">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="71948-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71948-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-1214">Az.Accounts</span></span>
* <span data-ttu-id="71948-1215">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1216">Az.Compute</span></span>
* <span data-ttu-id="71948-1217">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="71948-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="71948-1218">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="71948-1219">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="71948-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-1221">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="71948-1222">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71948-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71948-1223">Az.EventGrid</span></span>
* <span data-ttu-id="71948-1224">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="71948-1225">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="71948-1226">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="71948-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="71948-1227">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="71948-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="71948-1228">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="71948-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="71948-1229">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="71948-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="71948-1230">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="71948-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="71948-1231">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="71948-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="71948-1232">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="71948-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="71948-1233">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="71948-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="71948-1234">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="71948-1235">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="71948-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71948-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71948-1236">Az.IotHub</span></span>
* <span data-ttu-id="71948-1237">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71948-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71948-1238">Az.LogicApp</span></span>
* <span data-ttu-id="71948-1239">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="71948-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1240">Az.Resources</span></span>
* <span data-ttu-id="71948-1241">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="71948-1242">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="71948-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="71948-1243">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="71948-1244">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="71948-1245">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="71948-1246">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="71948-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71948-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71948-1247">Az.SignalR</span></span>
* <span data-ttu-id="71948-1248">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="71948-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1249">Az.Sql</span></span>
* <span data-ttu-id="71948-1250">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="71948-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71948-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-1251">Az.Storage</span></span>
* <span data-ttu-id="71948-1252">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="71948-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="71948-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="71948-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="71948-1254">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="71948-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="71948-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-1256">Az.Websites</span></span>
* <span data-ttu-id="71948-1257">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="71948-1258">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="71948-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="71948-1259">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="71948-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="71948-1260">Genel</span><span class="sxs-lookup"><span data-stu-id="71948-1260">General</span></span>

- <span data-ttu-id="71948-1261">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="71948-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="71948-1262">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="71948-1262">Online help for each module</span></span>
- <span data-ttu-id="71948-1263">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="71948-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="71948-1264">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="71948-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71948-1265">Az.Accounts</span></span>
- <span data-ttu-id="71948-1266">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71948-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="71948-1267">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="71948-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71948-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="71948-1269">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="71948-1269">Fixes for #7002</span></span>
- <span data-ttu-id="71948-1270">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="71948-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71948-1271">Az.Batch</span></span>
- <span data-ttu-id="71948-1272">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="71948-1273">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="71948-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="71948-1274">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="71948-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="71948-1275">Az.Billing</span></span>
- <span data-ttu-id="71948-1276">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="71948-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="71948-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="71948-1278">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="71948-1279">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="71948-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71948-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="71948-1281">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="71948-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="71948-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="71948-1283">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="71948-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="71948-1285">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="71948-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71948-1286">Az.Monitor</span></span>
- <span data-ttu-id="71948-1287">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="71948-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71948-1288">Az.KeyVault</span></span>
- <span data-ttu-id="71948-1289">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="71948-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="71948-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="71948-1291">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="71948-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="71948-1292">Az.Media</span></span>
- <span data-ttu-id="71948-1293">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="71948-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="71948-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1294">Az.Network</span></span>
<span data-ttu-id="71948-1295">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="71948-1296">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="71948-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="71948-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71948-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71948-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71948-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71948-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71948-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71948-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71948-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71948-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71948-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71948-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="71948-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="71948-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="71948-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="71948-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="71948-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="71948-1305">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="71948-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71948-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="71948-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71948-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="71948-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71948-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="71948-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71948-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="71948-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71948-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="71948-1311">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="71948-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="71948-1312">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="71948-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71948-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="71948-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71948-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="71948-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71948-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="71948-1316">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="71948-1317">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="71948-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71948-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="71948-1319">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="71948-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71948-1320">Az.Profile</span></span>
- <span data-ttu-id="71948-1321">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="71948-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="71948-1323">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="71948-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1324">Az.Resources</span></span>
- <span data-ttu-id="71948-1325">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="71948-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="71948-1327">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="71948-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="71948-1328">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="71948-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="71948-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="71948-1330">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="71948-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="71948-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1331">Az.Sql</span></span>
- <span data-ttu-id="71948-1332">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="71948-1333">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="71948-1334">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="71948-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-1335">Az.Storage</span></span>
- <span data-ttu-id="71948-1336">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="71948-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-1337">Az.Websites</span></span>
- <span data-ttu-id="71948-1338">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="71948-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="71948-1339">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="71948-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="71948-1340">Genel</span><span class="sxs-lookup"><span data-stu-id="71948-1340">General</span></span>

* <span data-ttu-id="71948-1341">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="71948-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="71948-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1342">Az.Compute</span></span>

* <span data-ttu-id="71948-1343">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="71948-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="71948-1345">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="71948-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71948-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="71948-1347">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="71948-1348">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="71948-1349">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="71948-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71948-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="71948-1351">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="71948-1352">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="71948-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1353">Az.Resources</span></span>

* <span data-ttu-id="71948-1354">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="71948-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="71948-1355">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="71948-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1356">Az.Sql</span></span>

* <span data-ttu-id="71948-1357">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="71948-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="71948-1358">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="71948-1359">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="71948-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71948-1360">Az.Storage</span></span>

* <span data-ttu-id="71948-1361">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="71948-1362">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="71948-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="71948-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="71948-1364">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="71948-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71948-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="71948-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71948-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="71948-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-1367">Az.Websites</span></span>

* <span data-ttu-id="71948-1368">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71948-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="71948-1369">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="71948-1370">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="71948-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="71948-1371">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="71948-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="71948-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71948-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="71948-1373">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="71948-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="71948-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71948-1374">Az.Automation</span></span>
* <span data-ttu-id="71948-1375">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="71948-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="71948-1376">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="71948-1377">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="71948-1378">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="71948-1379">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="71948-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1380">Az.Compute</span></span>
* <span data-ttu-id="71948-1381">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="71948-1382">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="71948-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="71948-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71948-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="71948-1384">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="71948-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="71948-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="71948-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="71948-1386">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="71948-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1387">Az.Network</span></span>
* <span data-ttu-id="71948-1388">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="71948-1389">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="71948-1390">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="71948-1391">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="71948-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="71948-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="71948-1393">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="71948-1394">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="71948-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="71948-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="71948-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="71948-1396">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="71948-1397">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="71948-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="71948-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="71948-1398">Az.Relay</span></span>
* <span data-ttu-id="71948-1399">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="71948-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1400">Az.Resources</span></span>
* <span data-ttu-id="71948-1401">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="71948-1402">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="71948-1403">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="71948-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="71948-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="71948-1405">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="71948-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1406">Az.Sql</span></span>
* <span data-ttu-id="71948-1407">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="71948-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71948-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71948-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71948-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71948-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71948-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71948-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71948-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71948-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71948-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71948-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71948-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71948-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71948-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71948-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="71948-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="71948-1416">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="71948-1417">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="71948-1418">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="71948-1419">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="71948-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="71948-1420">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="71948-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="71948-1421">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="71948-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="71948-1422">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="71948-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="71948-1423">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="71948-1424">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="71948-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="71948-1425">Genel</span><span class="sxs-lookup"><span data-stu-id="71948-1425">General</span></span>
* <span data-ttu-id="71948-1426">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="71948-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="71948-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71948-1427">Az.Profile</span></span>
* <span data-ttu-id="71948-1428">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="71948-1429">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="71948-1430">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="71948-1431">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="71948-1432">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="71948-1433">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="71948-1434">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="71948-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71948-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="71948-1436">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1437">Az.Compute</span></span>
* <span data-ttu-id="71948-1438">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="71948-1439">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="71948-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="71948-1440">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-1442">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="71948-1443">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="71948-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="71948-1444">Az.Insights</span></span>
* <span data-ttu-id="71948-1445">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="71948-1446">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="71948-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="71948-1447">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="71948-1448">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="71948-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1449">Az.Network</span></span>
* <span data-ttu-id="71948-1450">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="71948-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="71948-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="71948-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="71948-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="71948-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="71948-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="71948-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="71948-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="71948-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="71948-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="71948-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="71948-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="71948-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71948-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71948-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="71948-1458">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1459">Az.Resources</span></span>
* <span data-ttu-id="71948-1460">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="71948-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="71948-1461">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="71948-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71948-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71948-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="71948-1463">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71948-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71948-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="71948-1465">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="71948-1466">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="71948-1467">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="71948-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="71948-1468">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="71948-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="71948-1469">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="71948-1470">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="71948-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="71948-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71948-1471">Az.Profile</span></span>
* <span data-ttu-id="71948-1472">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="71948-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="71948-1473">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="71948-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1474">Az.Compute</span></span>
* <span data-ttu-id="71948-1475">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="71948-1476">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71948-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71948-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="71948-1478">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="71948-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="71948-1479">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="71948-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="71948-1480">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="71948-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="71948-1481">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="71948-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="71948-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="71948-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1483">Az.Network</span></span>
* <span data-ttu-id="71948-1484">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="71948-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="71948-1485">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1486">Az.Resources</span></span>
* <span data-ttu-id="71948-1487">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="71948-1488">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="71948-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="71948-1489">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="71948-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="71948-1490">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="71948-1490">Azure.Storage</span></span>
* <span data-ttu-id="71948-1491">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="71948-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="71948-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71948-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="71948-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="71948-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="71948-1494">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="71948-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="71948-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="71948-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="71948-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71948-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="71948-1497">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="71948-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71948-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71948-1498">Az.Compute</span></span>
* <span data-ttu-id="71948-1499">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="71948-1500">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="71948-1501">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="71948-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="71948-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="71948-1503">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="71948-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71948-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71948-1504">Az.Network</span></span>
* <span data-ttu-id="71948-1505">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="71948-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="71948-1506">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1506">new cmdlets added</span></span>
    - <span data-ttu-id="71948-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71948-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="71948-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71948-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="71948-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71948-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="71948-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71948-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="71948-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="71948-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="71948-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="71948-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="71948-1513">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="71948-1514">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="71948-1515">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71948-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71948-1516">Az.RedisCache</span></span>
* <span data-ttu-id="71948-1517">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="71948-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="71948-1518">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="71948-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71948-1519">Az.Resources</span></span>
* <span data-ttu-id="71948-1520">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="71948-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="71948-1521">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="71948-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71948-1522">Az.Sql</span></span>
* <span data-ttu-id="71948-1523">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="71948-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71948-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71948-1524">Az.Websites</span></span>
* <span data-ttu-id="71948-1525">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="71948-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="71948-1526">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="71948-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="71948-1527">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="71948-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="71948-1528">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="71948-1528">Initial Release</span></span>
