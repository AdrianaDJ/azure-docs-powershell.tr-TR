---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 656e61e7f208367fc7fae28f73d1b6f289831d77
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427743"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="ba30e-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="ba30e-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="ba30e-104">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ba30e-105">Genel</span><span class="sxs-lookup"><span data-stu-id="ba30e-105">General</span></span>
* <span data-ttu-id="ba30e-106">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="ba30e-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ba30e-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-107">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-108">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ba30e-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba30e-109">Az.ApiManagement</span></span>
* <span data-ttu-id="ba30e-110">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ba30e-111">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-112">Az.Automation</span></span>
* <span data-ttu-id="ba30e-113">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ba30e-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ba30e-114">Az.Batch</span></span>
* <span data-ttu-id="ba30e-115">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="ba30e-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-116">Az.Compute</span></span>
* <span data-ttu-id="ba30e-117">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ba30e-118">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ba30e-119">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="ba30e-120">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-121">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-122">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="ba30e-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ba30e-123">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="ba30e-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ba30e-124">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-126">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ba30e-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ba30e-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="ba30e-128">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ba30e-129">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ba30e-130">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ba30e-131">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ba30e-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-132">Az.IotHub</span></span>
* <span data-ttu-id="ba30e-133">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ba30e-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ba30e-134">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ba30e-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-135">Az.Monitor</span></span>
* <span data-ttu-id="ba30e-136">New-AzActionGroupReceiver için yeni eylem grubu alıcıları eklendi:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ba30e-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ba30e-137">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba30e-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ba30e-138">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="ba30e-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ba30e-139">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-140">Az.Network</span></span>
* <span data-ttu-id="ba30e-141">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ba30e-142">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ba30e-143">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-143">New cmdlets added:</span></span>
        - <span data-ttu-id="ba30e-144">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ba30e-145">Cmdlet’ler isteğe bağlı -TrafficSelectorPolicies parametresi ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="ba30e-146">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="ba30e-147">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ba30e-148">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ba30e-149">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="ba30e-150">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ba30e-151">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ba30e-152">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ba30e-153">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ba30e-154">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="ba30e-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ba30e-155">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="ba30e-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ba30e-156">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="ba30e-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ba30e-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ba30e-157">Az.RedisCache</span></span>
* <span data-ttu-id="ba30e-158">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-159">Az.Sql</span></span>
* <span data-ttu-id="ba30e-160">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-161">Az.Storage</span></span>
* <span data-ttu-id="ba30e-162">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ba30e-163">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="ba30e-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ba30e-164">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ba30e-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ba30e-165">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="ba30e-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ba30e-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ba30e-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ba30e-167">Az.StorageSync</span></span>
* <span data-ttu-id="ba30e-168">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-169">Az.Websites</span></span>
* <span data-ttu-id="ba30e-170">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ba30e-171">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ba30e-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba30e-172">Az.ApiManagement</span></span>
* <span data-ttu-id="ba30e-173">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ba30e-174">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ba30e-175">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba30e-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-176">Az.Automation</span></span>
* <span data-ttu-id="ba30e-177">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ba30e-178">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ba30e-179">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-180">Az.Compute</span></span>
* <span data-ttu-id="ba30e-181">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ba30e-182">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ba30e-183">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ba30e-184">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ba30e-185">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ba30e-186">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ba30e-187">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ba30e-188">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ba30e-189">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-190">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-191">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ba30e-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ba30e-192">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ba30e-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ba30e-193">Az.HDInsight</span></span>
* <span data-ttu-id="ba30e-194">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="ba30e-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ba30e-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-195">Az.IotHub</span></span>
* <span data-ttu-id="ba30e-196">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ba30e-197">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ba30e-198">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ba30e-198">New cmdlets are:</span></span>
    - <span data-ttu-id="ba30e-199">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ba30e-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ba30e-200">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ba30e-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ba30e-201">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ba30e-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ba30e-202">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ba30e-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ba30e-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-203">Az.Monitor</span></span>
* <span data-ttu-id="ba30e-204">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="ba30e-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ba30e-205">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ba30e-206">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="ba30e-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ba30e-207">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="ba30e-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ba30e-208">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ba30e-209">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ba30e-210">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ba30e-211">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="ba30e-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ba30e-212">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ba30e-213">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="ba30e-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ba30e-214">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ba30e-215">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="ba30e-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ba30e-216">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ba30e-217">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="ba30e-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ba30e-218">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="ba30e-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ba30e-219">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="ba30e-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ba30e-220">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="ba30e-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ba30e-221">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="ba30e-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ba30e-222">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ba30e-223">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-223">Overall improved help files</span></span>
* <span data-ttu-id="ba30e-224">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-225">Az.Network</span></span>
* <span data-ttu-id="ba30e-226">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="ba30e-227">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ba30e-228">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ba30e-229">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ba30e-230">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ba30e-231">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ba30e-232">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ba30e-233">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ba30e-234">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ba30e-235">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ba30e-236">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ba30e-237">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="ba30e-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ba30e-238">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-238">New cmdlets</span></span>
        - <span data-ttu-id="ba30e-239">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ba30e-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ba30e-240">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ba30e-241">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="ba30e-242">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ba30e-242">New-VpnSite</span></span>
        - <span data-ttu-id="ba30e-243">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ba30e-243">Update-VpnSite</span></span>
        - <span data-ttu-id="ba30e-244">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-244">New-VpnConnection</span></span>
        - <span data-ttu-id="ba30e-245">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-245">Update-VpnConnection</span></span>
* <span data-ttu-id="ba30e-246">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-248">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ba30e-249">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-250">Az.Resources</span></span>
* <span data-ttu-id="ba30e-251">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ba30e-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="ba30e-253">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ba30e-254">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="ba30e-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ba30e-255">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ba30e-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ba30e-256">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ba30e-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ba30e-257">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ba30e-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ba30e-258">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ba30e-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ba30e-259">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ba30e-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ba30e-260">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ba30e-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ba30e-261">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ba30e-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ba30e-262">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ba30e-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ba30e-263">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ba30e-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ba30e-264">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ba30e-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ba30e-265">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ba30e-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ba30e-266">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ba30e-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ba30e-267">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ba30e-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ba30e-268">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ba30e-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ba30e-269">Az.SignalR</span></span>
* <span data-ttu-id="ba30e-270">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-271">Az.Sql</span></span>
* <span data-ttu-id="ba30e-272">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ba30e-273">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ba30e-274">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ba30e-275">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ba30e-276">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-277">Az.Storage</span></span>
* <span data-ttu-id="ba30e-278">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ba30e-279">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ba30e-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ba30e-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ba30e-282">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ba30e-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ba30e-284">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ba30e-285">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ba30e-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ba30e-286">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ba30e-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ba30e-287">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ba30e-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ba30e-288">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ba30e-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-289">Az.Websites</span></span>
* <span data-ttu-id="ba30e-290">Uygulama yeni ASP’ye geçirilirken webapp etiketlerinin silinmesine neden olan sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ba30e-291">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ba30e-292">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ba30e-293">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ba30e-294">Genel</span><span class="sxs-lookup"><span data-stu-id="ba30e-294">General</span></span>
* <span data-ttu-id="ba30e-295">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ba30e-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-296">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-297">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="ba30e-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ba30e-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ba30e-298">Az.Aks</span></span>
* <span data-ttu-id="ba30e-299">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ba30e-300">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ba30e-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ba30e-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba30e-301">Az.ApiManagement</span></span>
* <span data-ttu-id="ba30e-302">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ba30e-303">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ba30e-304">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ba30e-305">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ba30e-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ba30e-306">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ba30e-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ba30e-307">Az.Batch</span></span>
* <span data-ttu-id="ba30e-308">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ba30e-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ba30e-309">Az.Cdn</span></span>
* <span data-ttu-id="ba30e-310">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-311">Az.Compute</span></span>
* <span data-ttu-id="ba30e-312">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ba30e-313">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ba30e-314">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ba30e-315">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ba30e-316">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ba30e-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ba30e-317">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ba30e-318">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ba30e-319">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-320">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-321">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ba30e-322">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ba30e-323">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ba30e-324">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-326">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ba30e-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-327">Az.EventHub</span></span>
* <span data-ttu-id="ba30e-328">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="ba30e-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ba30e-329">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="ba30e-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ba30e-330">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ba30e-331">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="ba30e-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ba30e-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ba30e-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ba30e-333">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ba30e-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-334">Az.Monitor</span></span>
* <span data-ttu-id="ba30e-335">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-336">Az.Network</span></span>
* <span data-ttu-id="ba30e-337">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ba30e-338">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ba30e-339">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ba30e-340">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="ba30e-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ba30e-341">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="ba30e-342">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ba30e-343">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ba30e-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="ba30e-345">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ba30e-346">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-346">Added example</span></span>
    - <span data-ttu-id="ba30e-347">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ba30e-348">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ba30e-349">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-351">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-352">Az.Resources</span></span>
* <span data-ttu-id="ba30e-353">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ba30e-354">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ba30e-355">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="ba30e-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ba30e-356">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ba30e-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba30e-357">Az.ServiceBus</span></span>
* <span data-ttu-id="ba30e-358">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="ba30e-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ba30e-359">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="ba30e-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ba30e-360">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ba30e-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="ba30e-362">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ba30e-363">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="ba30e-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ba30e-364">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ba30e-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ba30e-365">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ba30e-366">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ba30e-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ba30e-367">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-368">Az.Sql</span></span>
* <span data-ttu-id="ba30e-369">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-370">Az.Storage</span></span>
* <span data-ttu-id="ba30e-371">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ba30e-372">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="ba30e-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ba30e-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ba30e-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ba30e-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ba30e-375">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="ba30e-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ba30e-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ba30e-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-377">Az.Websites</span></span>
* <span data-ttu-id="ba30e-378">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ba30e-379">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-380">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-381">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ba30e-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ba30e-383">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-384">Az.Automation</span></span>
* <span data-ttu-id="ba30e-385">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ba30e-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="ba30e-387">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-388">Az.Compute</span></span>
* <span data-ttu-id="ba30e-389">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ba30e-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ba30e-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ba30e-391">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ba30e-392">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ba30e-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-393">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-394">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ba30e-395">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ba30e-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-396">Az.EventHub</span></span>
* <span data-ttu-id="ba30e-397">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ba30e-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ba30e-398">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ba30e-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba30e-399">Az.KeyVault</span></span>
* <span data-ttu-id="ba30e-400">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ba30e-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ba30e-401">Az.LogicApp</span></span>
* <span data-ttu-id="ba30e-402">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="ba30e-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ba30e-403">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ba30e-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-404">Az.ManagedServices</span></span>
* <span data-ttu-id="ba30e-405">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="ba30e-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-406">Az.Network</span></span>
* <span data-ttu-id="ba30e-407">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ba30e-408">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-408">New cmdlets</span></span>
        - <span data-ttu-id="ba30e-409">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba30e-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ba30e-410">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ba30e-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ba30e-411">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ba30e-412">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ba30e-413">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ba30e-414">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ba30e-415">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ba30e-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ba30e-416">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ba30e-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ba30e-417">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="ba30e-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ba30e-418">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ba30e-419">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ba30e-420">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ba30e-421">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ba30e-422">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ba30e-423">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-423">Updated cmdlets</span></span>
        - <span data-ttu-id="ba30e-424">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ba30e-425">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ba30e-426">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ba30e-427">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ba30e-428">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ba30e-429">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="ba30e-430">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ba30e-431">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ba30e-432">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ba30e-433">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ba30e-434">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ba30e-435">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="ba30e-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ba30e-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="ba30e-437">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="ba30e-438">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-440">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ba30e-441">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ba30e-442">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ba30e-443">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ba30e-444">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ba30e-445">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ba30e-446">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ba30e-447">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ba30e-448">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ba30e-449">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-450">Az.Resources</span></span>
- <span data-ttu-id="ba30e-451">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ba30e-452">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ba30e-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba30e-453">Az.ServiceBus</span></span>
* <span data-ttu-id="ba30e-454">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ba30e-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ba30e-455">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-456">Az.Sql</span></span>
* <span data-ttu-id="ba30e-457">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ba30e-458">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ba30e-459">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-460">Az.Storage</span></span>
* <span data-ttu-id="ba30e-461">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ba30e-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ba30e-462">Az.StorageSync</span></span>
* <span data-ttu-id="ba30e-463">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ba30e-464">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-465">Az.Websites</span></span>
* <span data-ttu-id="ba30e-466">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ba30e-467">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ba30e-468">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ba30e-469">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-470">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-471">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ba30e-472">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ba30e-473">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ba30e-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ba30e-474">Az.Advisor</span></span>
* <span data-ttu-id="ba30e-475">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ba30e-476">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="ba30e-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ba30e-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba30e-477">Az.ApiManagement</span></span>
* <span data-ttu-id="ba30e-478">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ba30e-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ba30e-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ba30e-480">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ba30e-481">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="ba30e-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ba30e-482">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="ba30e-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ba30e-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ba30e-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ba30e-484">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-485">Az.Automation</span></span>
* <span data-ttu-id="ba30e-486">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-487">Az.Compute</span></span>
* <span data-ttu-id="ba30e-488">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-489">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-490">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ba30e-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ba30e-491">Az.EventGrid</span></span>
* <span data-ttu-id="ba30e-492">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ba30e-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-493">Az.IotHub</span></span>
* <span data-ttu-id="ba30e-494">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-495">Az.Network</span></span>
* <span data-ttu-id="ba30e-496">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ba30e-497">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ba30e-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="ba30e-499">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ba30e-500">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ba30e-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ba30e-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="ba30e-502">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-504">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-505">Az.Resources</span></span>
    - <span data-ttu-id="ba30e-506">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ba30e-507">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ba30e-508">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ba30e-509">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ba30e-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba30e-510">Az.ServiceBus</span></span>
* <span data-ttu-id="ba30e-511">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-512">Az.Sql</span></span>
* <span data-ttu-id="ba30e-513">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ba30e-514">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ba30e-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ba30e-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ba30e-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ba30e-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ba30e-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ba30e-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ba30e-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ba30e-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ba30e-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ba30e-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ba30e-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ba30e-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ba30e-521">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-522">Az.Storage</span></span>
* <span data-ttu-id="ba30e-523">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ba30e-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ba30e-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ba30e-525">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ba30e-526">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ba30e-527">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ba30e-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ba30e-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ba30e-530">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ba30e-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ba30e-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ba30e-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ba30e-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ba30e-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ba30e-533">Az.StorageSync</span></span>
* <span data-ttu-id="ba30e-534">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="ba30e-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ba30e-535">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-536">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-537">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ba30e-538">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ba30e-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ba30e-539">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ba30e-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ba30e-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ba30e-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ba30e-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-542">Az.Compute</span></span>
* <span data-ttu-id="ba30e-543">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ba30e-544">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ba30e-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ba30e-545">Az.Dns</span></span>
* <span data-ttu-id="ba30e-546">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ba30e-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ba30e-547">Az.EventGrid</span></span>
* <span data-ttu-id="ba30e-548">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ba30e-549">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="ba30e-549">New cmdlets:</span></span>
    - <span data-ttu-id="ba30e-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ba30e-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ba30e-551">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba30e-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ba30e-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ba30e-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ba30e-553">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="ba30e-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ba30e-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ba30e-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ba30e-555">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba30e-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ba30e-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ba30e-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ba30e-557">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="ba30e-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ba30e-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ba30e-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ba30e-559">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ba30e-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ba30e-560">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ba30e-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ba30e-561">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba30e-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ba30e-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ba30e-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ba30e-563">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="ba30e-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="ba30e-564">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ba30e-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ba30e-565">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ba30e-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ba30e-566">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="ba30e-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ba30e-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ba30e-568">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ba30e-569">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ba30e-570">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ba30e-571">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ba30e-572">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="ba30e-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ba30e-573">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="ba30e-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ba30e-574">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ba30e-575">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="ba30e-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="ba30e-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ba30e-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ba30e-577">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ba30e-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ba30e-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ba30e-579">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ba30e-580">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ba30e-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ba30e-581">Az.FrontDoor</span></span>
* <span data-ttu-id="ba30e-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ba30e-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ba30e-583">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="ba30e-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ba30e-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ba30e-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ba30e-585">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="ba30e-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-586">Az.Network</span></span>
* <span data-ttu-id="ba30e-587">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="ba30e-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ba30e-588">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-588">New cmdlets</span></span>
        - <span data-ttu-id="ba30e-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ba30e-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ba30e-590">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="ba30e-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ba30e-591">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-591">New cmdlets</span></span>
        - <span data-ttu-id="ba30e-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ba30e-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ba30e-593">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="ba30e-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ba30e-594">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-594">New cmdlets</span></span>
        - <span data-ttu-id="ba30e-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ba30e-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ba30e-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ba30e-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ba30e-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ba30e-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ba30e-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ba30e-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ba30e-600">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="ba30e-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ba30e-601">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-601">New cmdlets</span></span>
        - <span data-ttu-id="ba30e-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba30e-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ba30e-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba30e-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ba30e-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba30e-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ba30e-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ba30e-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ba30e-606">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="ba30e-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ba30e-607">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ba30e-608">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ba30e-609">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ba30e-610">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ba30e-611">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ba30e-612">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ba30e-613">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ba30e-614">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ba30e-615">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ba30e-616">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ba30e-617">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ba30e-618">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ba30e-619">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ba30e-620">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ba30e-621">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ba30e-622">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ba30e-623">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ba30e-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ba30e-624">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ba30e-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="ba30e-625">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="ba30e-626">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ba30e-627">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ba30e-628">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ba30e-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="ba30e-630">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-631">Az.Resources</span></span>
* <span data-ttu-id="ba30e-632">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="ba30e-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ba30e-633">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ba30e-634">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ba30e-635">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ba30e-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="ba30e-637">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-638">Az.Sql</span></span>
* <span data-ttu-id="ba30e-639">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ba30e-640">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ba30e-641">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ba30e-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ba30e-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ba30e-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ba30e-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ba30e-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ba30e-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ba30e-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ba30e-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ba30e-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ba30e-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-647">Az.Storage</span></span>
* <span data-ttu-id="ba30e-648">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="ba30e-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ba30e-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="ba30e-650">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ba30e-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-652">Az.Websites</span></span>
* <span data-ttu-id="ba30e-653">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="ba30e-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ba30e-654">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="ba30e-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ba30e-655">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ba30e-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ba30e-656">Az.Cdn</span></span>
* <span data-ttu-id="ba30e-657">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-658">Az.Compute</span></span>
* <span data-ttu-id="ba30e-659">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ba30e-660">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ba30e-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ba30e-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-661">Az.EventHub</span></span>
* <span data-ttu-id="ba30e-662">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ba30e-663">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-664">Az.Network</span></span>
* <span data-ttu-id="ba30e-665">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ba30e-666">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ba30e-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="ba30e-668">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-670">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ba30e-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba30e-671">Az.ServiceBus</span></span>
* <span data-ttu-id="ba30e-672">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="ba30e-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ba30e-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="ba30e-674">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ba30e-675">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-676">Az.Sql</span></span>
* <span data-ttu-id="ba30e-677">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ba30e-678">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ba30e-679">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ba30e-680">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-681">Az.Websites</span></span>
* <span data-ttu-id="ba30e-682">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ba30e-683">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ba30e-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba30e-684">Az.ApiManagement</span></span>
* <span data-ttu-id="ba30e-685">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ba30e-686">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="ba30e-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ba30e-687">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="ba30e-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ba30e-688">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="ba30e-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ba30e-689">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba30e-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ba30e-690">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="ba30e-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ba30e-691">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="ba30e-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ba30e-692">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="ba30e-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ba30e-693">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ba30e-694">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="ba30e-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ba30e-695">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="ba30e-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ba30e-696">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="ba30e-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ba30e-697">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="ba30e-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ba30e-698">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ba30e-699">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="ba30e-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ba30e-700">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="ba30e-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ba30e-701">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="ba30e-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ba30e-702">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="ba30e-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ba30e-703">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="ba30e-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="ba30e-704">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="ba30e-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ba30e-705">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ba30e-706">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ba30e-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ba30e-707">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="ba30e-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ba30e-708">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="ba30e-709">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ba30e-710">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ba30e-711">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ba30e-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ba30e-712">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ba30e-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ba30e-713">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ba30e-714">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ba30e-715">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="ba30e-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ba30e-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ba30e-717">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ba30e-718">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ba30e-719">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ba30e-720">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="ba30e-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ba30e-721">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="ba30e-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ba30e-722">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ba30e-723">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ba30e-724">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ba30e-725">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="ba30e-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ba30e-726">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ba30e-727">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="ba30e-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ba30e-728">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ba30e-729">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ba30e-730">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="ba30e-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ba30e-731">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="ba30e-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ba30e-732">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ba30e-733">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ba30e-734">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="ba30e-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ba30e-735">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="ba30e-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ba30e-736">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ba30e-737">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="ba30e-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ba30e-738">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ba30e-739">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ba30e-740">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ba30e-741">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ba30e-742">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ba30e-743">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ba30e-744">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ba30e-745">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ba30e-746">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ba30e-747">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="ba30e-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ba30e-748">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ba30e-749">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ba30e-750">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="ba30e-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ba30e-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ba30e-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ba30e-752">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="ba30e-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ba30e-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ba30e-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ba30e-754">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ba30e-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ba30e-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ba30e-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ba30e-756">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ba30e-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ba30e-757">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="ba30e-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ba30e-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ba30e-759">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="ba30e-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="ba30e-760">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ba30e-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ba30e-761">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="ba30e-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-762">Az.Automation</span></span>
* <span data-ttu-id="ba30e-763">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ba30e-764">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ba30e-765">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ba30e-766">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ba30e-767">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ba30e-768">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ba30e-769">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-770">Az.Compute</span></span>
* <span data-ttu-id="ba30e-771">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ba30e-772">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-774">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ba30e-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-775">Az.Monitor</span></span>
* <span data-ttu-id="ba30e-776">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-777">Az.Network</span></span>
* <span data-ttu-id="ba30e-778">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ba30e-779">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="ba30e-780">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ba30e-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ba30e-781">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-782">Az.Resources</span></span>
* <span data-ttu-id="ba30e-783">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-784">Az.Sql</span></span>
* <span data-ttu-id="ba30e-785">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ba30e-786">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-787">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-788">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="ba30e-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ba30e-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="ba30e-790">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ba30e-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ba30e-791">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="ba30e-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-792">Az.Compute</span></span>
* <span data-ttu-id="ba30e-793">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ba30e-794">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ba30e-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ba30e-795">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ba30e-796">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ba30e-797">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="ba30e-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ba30e-798">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="ba30e-799">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="ba30e-799">Breaking changes</span></span>
    - <span data-ttu-id="ba30e-800">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ba30e-801">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ba30e-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ba30e-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="ba30e-803">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="ba30e-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ba30e-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ba30e-804">Az.Dns</span></span>
* <span data-ttu-id="ba30e-805">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="ba30e-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ba30e-806">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="ba30e-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ba30e-807">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ba30e-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ba30e-808">Az.FrontDoor</span></span>
* <span data-ttu-id="ba30e-809">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="ba30e-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ba30e-810">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="ba30e-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ba30e-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ba30e-811">Az.HDInsight</span></span>
* <span data-ttu-id="ba30e-812">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="ba30e-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ba30e-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ba30e-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ba30e-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ba30e-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ba30e-815">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ba30e-816">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="ba30e-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ba30e-817">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="ba30e-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ba30e-818">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="ba30e-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ba30e-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-819">Az.Monitor</span></span>
* <span data-ttu-id="ba30e-820">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="ba30e-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ba30e-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ba30e-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ba30e-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ba30e-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ba30e-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ba30e-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ba30e-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ba30e-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ba30e-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ba30e-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ba30e-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ba30e-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ba30e-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ba30e-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ba30e-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ba30e-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ba30e-832">SQR API hakkında [daha fazla](/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="ba30e-832">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ba30e-833">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-834">Az.Network</span></span>
* <span data-ttu-id="ba30e-835">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="ba30e-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ba30e-836">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-836">New cmdlets</span></span>
        - <span data-ttu-id="ba30e-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ba30e-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="ba30e-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ba30e-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ba30e-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ba30e-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ba30e-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ba30e-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ba30e-841">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-841">Updated cmdlets</span></span>
        - <span data-ttu-id="ba30e-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ba30e-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ba30e-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ba30e-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ba30e-844">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="ba30e-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ba30e-845">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ba30e-846">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ba30e-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="ba30e-848">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ba30e-849">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ba30e-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ba30e-850">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="ba30e-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-852">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ba30e-853">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="ba30e-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ba30e-854">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="ba30e-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ba30e-855">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="ba30e-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ba30e-856">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="ba30e-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ba30e-857">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ba30e-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ba30e-858">Az.Relay</span></span>
* <span data-ttu-id="ba30e-859">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="ba30e-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ba30e-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba30e-860">Az.ServiceBus</span></span>
* <span data-ttu-id="ba30e-861">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-862">Az.Storage</span></span>
* <span data-ttu-id="ba30e-863">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="ba30e-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ba30e-864">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ba30e-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ba30e-865">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="ba30e-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ba30e-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="ba30e-867">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="ba30e-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ba30e-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ba30e-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ba30e-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-871">Az.Websites</span></span>
* <span data-ttu-id="ba30e-872">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="ba30e-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ba30e-873">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ba30e-874">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ba30e-875">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="ba30e-875">Highlights since the last major release</span></span>
* <span data-ttu-id="ba30e-876">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-876">General availability of `Az` module</span></span>
* <span data-ttu-id="ba30e-877">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ba30e-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ba30e-878">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ba30e-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ba30e-879">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ba30e-880">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ba30e-881">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ba30e-882">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ba30e-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-883">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-884">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ba30e-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ba30e-885">Az.Batch</span></span>
* <span data-ttu-id="ba30e-886">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ba30e-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ba30e-887">Az.Cdn</span></span>
* <span data-ttu-id="ba30e-888">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ba30e-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="ba30e-890">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-891">Az.Compute</span></span>
* <span data-ttu-id="ba30e-892">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ba30e-893">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ba30e-894">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-895">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-896">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-898">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ba30e-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ba30e-899">Az.EventGrid</span></span>
* <span data-ttu-id="ba30e-900">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ba30e-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-901">Az.EventHub</span></span>
* <span data-ttu-id="ba30e-902">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ba30e-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ba30e-903">Az.HDInsight</span></span>
* <span data-ttu-id="ba30e-904">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ba30e-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-905">Az.IotHub</span></span>
* <span data-ttu-id="ba30e-906">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ba30e-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba30e-907">Az.KeyVault</span></span>
* <span data-ttu-id="ba30e-908">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ba30e-909">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ba30e-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ba30e-910">Az.MachineLearning</span></span>
* <span data-ttu-id="ba30e-911">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ba30e-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ba30e-912">Az.Media</span></span>
* <span data-ttu-id="ba30e-913">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ba30e-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-914">Az.Monitor</span></span>
  * <span data-ttu-id="ba30e-915">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ba30e-916">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ba30e-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ba30e-917">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ba30e-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ba30e-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ba30e-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ba30e-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ba30e-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ba30e-920">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ba30e-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ba30e-921">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-922">Az.Network</span></span>
* <span data-ttu-id="ba30e-923">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ba30e-924">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ba30e-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ba30e-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="ba30e-926">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ba30e-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="ba30e-928">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ba30e-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ba30e-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ba30e-930">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-932">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ba30e-933">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="ba30e-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ba30e-934">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ba30e-935">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ba30e-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ba30e-936">Az.RedisCache</span></span>
* <span data-ttu-id="ba30e-937">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-938">Az.Resources</span></span>
* <span data-ttu-id="ba30e-939">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-940">Az.Sql</span></span>
* <span data-ttu-id="ba30e-941">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ba30e-942">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ba30e-943">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ba30e-944">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ba30e-945">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ba30e-946">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ba30e-947">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-948">Az.Websites</span></span>
* <span data-ttu-id="ba30e-949">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ba30e-950">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ba30e-951">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ba30e-952">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ba30e-953">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ba30e-954">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="ba30e-954">Highlights since the last major release</span></span>
* <span data-ttu-id="ba30e-955">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-955">General availability of `Az` module</span></span>
* <span data-ttu-id="ba30e-956">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ba30e-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ba30e-957">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ba30e-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ba30e-958">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ba30e-959">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ba30e-960">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ba30e-961">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ba30e-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-962">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-963">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ba30e-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="ba30e-965">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ba30e-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ba30e-966">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="ba30e-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-967">Az.Automation</span></span>
* <span data-ttu-id="ba30e-968">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ba30e-969">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ba30e-970">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-971">Az.Compute</span></span>
* <span data-ttu-id="ba30e-972">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ba30e-973">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ba30e-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ba30e-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="ba30e-975">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-976">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-977">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ba30e-978">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-979">Az.Resources</span></span>
* <span data-ttu-id="ba30e-980">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ba30e-981">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ba30e-982">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ba30e-983">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ba30e-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ba30e-984">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ba30e-985">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ba30e-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-986">Az.Sql</span></span>
* <span data-ttu-id="ba30e-987">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-988">Az.Storage</span></span>
* <span data-ttu-id="ba30e-989">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="ba30e-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ba30e-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ba30e-990">New-AzStorageContext</span></span>
* <span data-ttu-id="ba30e-991">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="ba30e-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ba30e-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ba30e-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ba30e-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ba30e-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ba30e-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ba30e-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ba30e-996">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="ba30e-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ba30e-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ba30e-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ba30e-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ba30e-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ba30e-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ba30e-1001">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ba30e-1002">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="ba30e-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="ba30e-1003">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="ba30e-1004">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ba30e-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ba30e-1005">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ba30e-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ba30e-1006">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ba30e-1007">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ba30e-1008">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ba30e-1009">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-1010">Az.Automation</span></span>
* <span data-ttu-id="ba30e-1011">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="ba30e-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ba30e-1012">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="ba30e-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="ba30e-1013">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="ba30e-1013">Pre-Post script</span></span>
    * <span data-ttu-id="ba30e-1014">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1015">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1016">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="ba30e-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ba30e-1017">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ba30e-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba30e-1018">Az.KeyVault</span></span>
* <span data-ttu-id="ba30e-1019">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1020">Az.Network</span></span>
* <span data-ttu-id="ba30e-1021">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ba30e-1022">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-1024">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ba30e-1025">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1026">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1027">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ba30e-1028">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1029">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1030">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-1031">Az.Storage</span></span>
* <span data-ttu-id="ba30e-1032">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="ba30e-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ba30e-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ba30e-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ba30e-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ba30e-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ba30e-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ba30e-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ba30e-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ba30e-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-1039">Az.Websites</span></span>
* <span data-ttu-id="ba30e-1040">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="ba30e-1041">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-1042">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-1043">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ba30e-1044">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-1045">Az.Automation</span></span>
* <span data-ttu-id="ba30e-1046">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ba30e-1047">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ba30e-1048">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="ba30e-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ba30e-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ba30e-1049">Az.Cdn</span></span>
* <span data-ttu-id="ba30e-1050">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1051">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1052">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-1053">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-1054">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ba30e-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ba30e-1055">Az.LogicApp</span></span>
* <span data-ttu-id="ba30e-1056">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="ba30e-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1057">Az.Network</span></span>
* <span data-ttu-id="ba30e-1058">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-1060">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ba30e-1061">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1061">SDK Update</span></span>
* <span data-ttu-id="ba30e-1062">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ba30e-1063">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1064">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1065">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ba30e-1066">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ba30e-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ba30e-1067">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ba30e-1068">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ba30e-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ba30e-1069">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ba30e-1070">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ba30e-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1071">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1072">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ba30e-1073">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-1074">Az.Storage</span></span>
* <span data-ttu-id="ba30e-1075">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba30e-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ba30e-1076">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ba30e-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="ba30e-1078">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-1079">Az.Automation</span></span>
* <span data-ttu-id="ba30e-1080">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ba30e-1081">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ba30e-1082">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ba30e-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="ba30e-1084">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1085">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1086">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ba30e-1087">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ba30e-1088">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ba30e-1089">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-1091">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ba30e-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-1092">Az.EventHub</span></span>
* <span data-ttu-id="ba30e-1093">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ba30e-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba30e-1094">Az.KeyVault</span></span>
* <span data-ttu-id="ba30e-1095">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ba30e-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ba30e-1096">Az.LogicApp</span></span>
* <span data-ttu-id="ba30e-1097">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ba30e-1098">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ba30e-1099">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ba30e-1100">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ba30e-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ba30e-1101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ba30e-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ba30e-1102">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ba30e-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ba30e-1103">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ba30e-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ba30e-1104">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="ba30e-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ba30e-1105">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba30e-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ba30e-1106">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba30e-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ba30e-1107">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba30e-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ba30e-1108">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba30e-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ba30e-1109">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ba30e-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1110">Az.Monitor</span></span>
* <span data-ttu-id="ba30e-1111">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1112">Az.Network</span></span>
* <span data-ttu-id="ba30e-1113">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ba30e-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="ba30e-1115">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ba30e-1116">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="ba30e-1117">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1118">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1119">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ba30e-1120">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ba30e-1121">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ba30e-1122">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1123">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1124">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ba30e-1125">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-1126">Az.Websites</span></span>
* <span data-ttu-id="ba30e-1127">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ba30e-1128">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-1129">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-1130">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ba30e-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ba30e-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="ba30e-1132">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1133">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1134">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ba30e-1135">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ba30e-1136">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="ba30e-1138">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1139">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1140">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="ba30e-1141">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ba30e-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ba30e-1142">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="ba30e-1143">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ba30e-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1144">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba30e-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ba30e-1146">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ba30e-1147">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ba30e-1148">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-1149">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-1150">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="ba30e-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ba30e-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="ba30e-1152">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="ba30e-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="ba30e-1154">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="ba30e-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ba30e-1155">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-1156">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-1157">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ba30e-1158">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ba30e-1159">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ba30e-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ba30e-1160">Az.Aks</span></span>
* <span data-ttu-id="ba30e-1161">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ba30e-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-1162">Az.Automation</span></span>
* <span data-ttu-id="ba30e-1163">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ba30e-1164">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ba30e-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ba30e-1165">Az.Cdn</span></span>
* <span data-ttu-id="ba30e-1166">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1167">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1168">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ba30e-1169">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ba30e-1170">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ba30e-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ba30e-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ba30e-1172">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ba30e-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba30e-1173">Az.DataFactory</span></span>
* <span data-ttu-id="ba30e-1174">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-1176">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ba30e-1177">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ba30e-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ba30e-1178">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ba30e-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-1179">Az.IotHub</span></span>
* <span data-ttu-id="ba30e-1180">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ba30e-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba30e-1181">Az.KeyVault</span></span>
* <span data-ttu-id="ba30e-1182">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1183">Az.Network</span></span>
* <span data-ttu-id="ba30e-1184">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1185">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1186">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ba30e-1187">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ba30e-1188">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ba30e-1189">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ba30e-1190">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ba30e-1191">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ba30e-1192">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ba30e-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ba30e-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="ba30e-1194">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ba30e-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ba30e-1195">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1195">Fix some error messages.</span></span>
* <span data-ttu-id="ba30e-1196">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ba30e-1197">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ba30e-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ba30e-1198">Az.SignalR</span></span>
* <span data-ttu-id="ba30e-1199">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1200">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1201">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ba30e-1202">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ba30e-1203">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ba30e-1204">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="ba30e-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-1205">Az.Storage</span></span>
* <span data-ttu-id="ba30e-1206">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ba30e-1207">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ba30e-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ba30e-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ba30e-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ba30e-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ba30e-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ba30e-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="ba30e-1211">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-1212">Az.Websites</span></span>
* <span data-ttu-id="ba30e-1213">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ba30e-1214">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ba30e-1215">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ba30e-1216">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="ba30e-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ba30e-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-1217">Az.Accounts</span></span>
* <span data-ttu-id="ba30e-1218">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1219">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1220">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ba30e-1221">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ba30e-1222">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="ba30e-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-1224">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ba30e-1225">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ba30e-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ba30e-1226">Az.EventGrid</span></span>
* <span data-ttu-id="ba30e-1227">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ba30e-1228">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ba30e-1229">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ba30e-1230">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="ba30e-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ba30e-1231">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="ba30e-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ba30e-1232">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ba30e-1233">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ba30e-1234">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="ba30e-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ba30e-1235">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="ba30e-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ba30e-1236">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="ba30e-1237">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ba30e-1238">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ba30e-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba30e-1239">Az.IotHub</span></span>
* <span data-ttu-id="ba30e-1240">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ba30e-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ba30e-1241">Az.LogicApp</span></span>
* <span data-ttu-id="ba30e-1242">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1243">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1244">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ba30e-1245">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ba30e-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ba30e-1246">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ba30e-1247">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ba30e-1248">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ba30e-1249">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ba30e-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ba30e-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ba30e-1250">Az.SignalR</span></span>
* <span data-ttu-id="ba30e-1251">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="ba30e-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1252">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1253">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ba30e-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-1254">Az.Storage</span></span>
* <span data-ttu-id="ba30e-1255">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ba30e-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ba30e-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="ba30e-1257">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ba30e-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ba30e-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-1259">Az.Websites</span></span>
* <span data-ttu-id="ba30e-1260">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ba30e-1261">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="ba30e-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ba30e-1262">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="ba30e-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ba30e-1263">Genel</span><span class="sxs-lookup"><span data-stu-id="ba30e-1263">General</span></span>

- <span data-ttu-id="ba30e-1264">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="ba30e-1265">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="ba30e-1265">Online help for each module</span></span>
- <span data-ttu-id="ba30e-1266">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ba30e-1267">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ba30e-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ba30e-1268">Az.Accounts</span></span>
- <span data-ttu-id="ba30e-1269">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="ba30e-1270">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ba30e-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba30e-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="ba30e-1272">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="ba30e-1272">Fixes for #7002</span></span>
- <span data-ttu-id="ba30e-1273">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ba30e-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ba30e-1274">Az.Batch</span></span>
- <span data-ttu-id="ba30e-1275">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ba30e-1276">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ba30e-1277">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ba30e-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ba30e-1278">Az.Billing</span></span>
- <span data-ttu-id="ba30e-1279">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ba30e-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="ba30e-1281">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ba30e-1282">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ba30e-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ba30e-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="ba30e-1284">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ba30e-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ba30e-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ba30e-1286">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="ba30e-1288">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ba30e-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1289">Az.Monitor</span></span>
- <span data-ttu-id="ba30e-1290">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ba30e-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba30e-1291">Az.KeyVault</span></span>
- <span data-ttu-id="ba30e-1292">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ba30e-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ba30e-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="ba30e-1294">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ba30e-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ba30e-1295">Az.Media</span></span>
- <span data-ttu-id="ba30e-1296">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ba30e-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1297">Az.Network</span></span>
<span data-ttu-id="ba30e-1298">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ba30e-1299">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="ba30e-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="ba30e-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba30e-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ba30e-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba30e-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ba30e-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba30e-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ba30e-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba30e-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ba30e-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba30e-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ba30e-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ba30e-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ba30e-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ba30e-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba30e-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ba30e-1308">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ba30e-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba30e-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ba30e-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ba30e-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ba30e-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ba30e-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ba30e-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ba30e-1314">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ba30e-1315">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ba30e-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba30e-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ba30e-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba30e-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ba30e-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ba30e-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ba30e-1319">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ba30e-1320">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ba30e-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="ba30e-1322">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ba30e-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1323">Az.Profile</span></span>
- <span data-ttu-id="ba30e-1324">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="ba30e-1326">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ba30e-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1327">Az.Resources</span></span>
- <span data-ttu-id="ba30e-1328">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ba30e-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="ba30e-1330">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="ba30e-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ba30e-1331">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ba30e-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ba30e-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="ba30e-1333">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="ba30e-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ba30e-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1334">Az.Sql</span></span>
- <span data-ttu-id="ba30e-1335">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ba30e-1336">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ba30e-1337">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ba30e-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-1338">Az.Storage</span></span>
- <span data-ttu-id="ba30e-1339">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ba30e-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-1340">Az.Websites</span></span>
- <span data-ttu-id="ba30e-1341">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ba30e-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ba30e-1342">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="ba30e-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ba30e-1343">Genel</span><span class="sxs-lookup"><span data-stu-id="ba30e-1343">General</span></span>

* <span data-ttu-id="ba30e-1344">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="ba30e-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ba30e-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1345">Az.Compute</span></span>

* <span data-ttu-id="ba30e-1346">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="ba30e-1348">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ba30e-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="ba30e-1350">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="ba30e-1351">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ba30e-1352">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ba30e-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="ba30e-1354">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ba30e-1355">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ba30e-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1356">Az.Resources</span></span>

* <span data-ttu-id="ba30e-1357"> https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ba30e-1358">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ba30e-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1359">Az.Sql</span></span>

* <span data-ttu-id="ba30e-1360">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="ba30e-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ba30e-1361">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ba30e-1362">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ba30e-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ba30e-1363">Az.Storage</span></span>

* <span data-ttu-id="ba30e-1364">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ba30e-1365">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ba30e-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ba30e-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ba30e-1367">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="ba30e-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ba30e-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ba30e-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ba30e-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ba30e-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-1370">Az.Websites</span></span>

* <span data-ttu-id="ba30e-1371">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ba30e-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="ba30e-1372">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ba30e-1373">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ba30e-1374">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="ba30e-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ba30e-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba30e-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="ba30e-1376">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="ba30e-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ba30e-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ba30e-1377">Az.Automation</span></span>
* <span data-ttu-id="ba30e-1378">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="ba30e-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ba30e-1379">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ba30e-1380">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ba30e-1381">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ba30e-1382">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ba30e-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1383">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1384">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ba30e-1385">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="ba30e-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ba30e-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ba30e-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="ba30e-1387">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="ba30e-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ba30e-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ba30e-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ba30e-1389">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ba30e-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1390">Az.Network</span></span>
* <span data-ttu-id="ba30e-1391">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ba30e-1392">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ba30e-1393">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="ba30e-1394">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ba30e-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ba30e-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ba30e-1396">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ba30e-1397">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ba30e-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ba30e-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ba30e-1399">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ba30e-1400">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="ba30e-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ba30e-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ba30e-1401">Az.Relay</span></span>
* <span data-ttu-id="ba30e-1402">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ba30e-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1403">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1404">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ba30e-1405">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ba30e-1406">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ba30e-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ba30e-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="ba30e-1408">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ba30e-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1409">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1410">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ba30e-1411">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ba30e-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ba30e-1412">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ba30e-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ba30e-1413">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ba30e-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ba30e-1414">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ba30e-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ba30e-1415">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ba30e-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ba30e-1416">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ba30e-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ba30e-1417">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ba30e-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ba30e-1418">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ba30e-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ba30e-1419">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ba30e-1420">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ba30e-1421">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ba30e-1422">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ba30e-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ba30e-1424">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ba30e-1425">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ba30e-1426">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ba30e-1427">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="ba30e-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ba30e-1428">Genel</span><span class="sxs-lookup"><span data-stu-id="ba30e-1428">General</span></span>
* <span data-ttu-id="ba30e-1429">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="ba30e-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ba30e-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1430">Az.Profile</span></span>
* <span data-ttu-id="ba30e-1431">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ba30e-1432">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ba30e-1433">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ba30e-1434">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ba30e-1435">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ba30e-1436">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ba30e-1437">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ba30e-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="ba30e-1439">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1440">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1441">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ba30e-1442">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ba30e-1443">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-1445">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ba30e-1446">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ba30e-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ba30e-1447">Az.Insights</span></span>
* <span data-ttu-id="ba30e-1448">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ba30e-1449">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="ba30e-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ba30e-1450">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ba30e-1451">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1452">Az.Network</span></span>
* <span data-ttu-id="ba30e-1453">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="ba30e-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ba30e-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ba30e-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ba30e-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ba30e-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ba30e-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ba30e-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ba30e-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ba30e-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ba30e-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ba30e-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ba30e-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ba30e-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ba30e-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ba30e-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="ba30e-1461">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1462">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1463"> https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ba30e-1464">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="ba30e-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ba30e-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba30e-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="ba30e-1466">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ba30e-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba30e-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="ba30e-1468">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ba30e-1469">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ba30e-1470">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ba30e-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ba30e-1471">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ba30e-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ba30e-1472">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ba30e-1473">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="ba30e-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ba30e-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1474">Az.Profile</span></span>
* <span data-ttu-id="ba30e-1475">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="ba30e-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ba30e-1476">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1477">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1478">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ba30e-1479">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ba30e-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba30e-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="ba30e-1481">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="ba30e-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ba30e-1482">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ba30e-1483">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ba30e-1484">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ba30e-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1486">Az.Network</span></span>
* <span data-ttu-id="ba30e-1487">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ba30e-1488">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1489">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1490">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ba30e-1491">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ba30e-1492">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="ba30e-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ba30e-1493">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="ba30e-1493">Azure.Storage</span></span>
* <span data-ttu-id="ba30e-1494">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="ba30e-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ba30e-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ba30e-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ba30e-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ba30e-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ba30e-1497">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ba30e-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ba30e-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ba30e-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ba30e-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="ba30e-1500">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ba30e-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ba30e-1501">Az.Compute</span></span>
* <span data-ttu-id="ba30e-1502">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ba30e-1503">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ba30e-1504">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ba30e-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ba30e-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ba30e-1506">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ba30e-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ba30e-1507">Az.Network</span></span>
* <span data-ttu-id="ba30e-1508">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ba30e-1509">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1509">new cmdlets added</span></span>
    - <span data-ttu-id="ba30e-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ba30e-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ba30e-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ba30e-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ba30e-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ba30e-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ba30e-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ba30e-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ba30e-1516">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ba30e-1517">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ba30e-1518">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ba30e-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ba30e-1519">Az.RedisCache</span></span>
* <span data-ttu-id="ba30e-1520">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="ba30e-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ba30e-1521">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ba30e-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ba30e-1522">Az.Resources</span></span>
* <span data-ttu-id="ba30e-1523">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ba30e-1524">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ba30e-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ba30e-1525">Az.Sql</span></span>
* <span data-ttu-id="ba30e-1526">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ba30e-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ba30e-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ba30e-1527">Az.Websites</span></span>
* <span data-ttu-id="ba30e-1528">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ba30e-1529">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="ba30e-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ba30e-1530">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="ba30e-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ba30e-1531">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="ba30e-1531">Initial Release</span></span>