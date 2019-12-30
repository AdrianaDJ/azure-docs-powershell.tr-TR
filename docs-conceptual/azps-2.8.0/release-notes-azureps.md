---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035770"
---
## <a name="280---october-2019"></a><span data-ttu-id="3a2e4-103">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="3a2e4-104">Genel</span><span class="sxs-lookup"><span data-stu-id="3a2e4-104">General</span></span>
* <span data-ttu-id="3a2e4-105">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-106">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-107">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3a2e4-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a2e4-108">Az.ApiManagement</span></span>
* <span data-ttu-id="3a2e4-109">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="3a2e4-110">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-111">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-112">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="3a2e4-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a2e4-113">Az.Batch</span></span>
* <span data-ttu-id="3a2e4-114">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-115">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-116">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="3a2e4-117">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="3a2e4-118">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="3a2e4-119">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-120">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-121">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="3a2e4-122">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="3a2e4-123">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-125">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3a2e4-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3a2e4-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="3a2e4-127">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="3a2e4-128">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="3a2e4-129">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="3a2e4-130">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a2e4-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-131">Az.IotHub</span></span>
* <span data-ttu-id="3a2e4-132">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="3a2e4-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="3a2e4-133">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="3a2e4-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-134">Az.Monitor</span></span>
* <span data-ttu-id="3a2e4-135">New-AzActionGroupReceiver için yeni eylem grubu alıcıları eklendi:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="3a2e4-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="3a2e4-136">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="3a2e4-137">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="3a2e4-138">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-139">Az.Network</span></span>
* <span data-ttu-id="3a2e4-140">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="3a2e4-141">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="3a2e4-142">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-142">New cmdlets added:</span></span>
        - <span data-ttu-id="3a2e4-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="3a2e4-144">Cmdlet’ler isteğe bağlı -TrafficSelectorPolicies parametresi ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="3a2e4-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="3a2e4-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3a2e4-147">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="3a2e4-148">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="3a2e4-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a2e4-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a2e4-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3a2e4-152">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="3a2e4-153">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="3a2e4-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="3a2e4-154">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="3a2e4-155">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a2e4-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a2e4-156">Az.RedisCache</span></span>
* <span data-ttu-id="3a2e4-157">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-158">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-159">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-160">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-161">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="3a2e4-162">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="3a2e4-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3a2e4-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a2e4-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="3a2e4-164">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="3a2e4-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3a2e4-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3a2e4-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3a2e4-166">Az.StorageSync</span></span>
* <span data-ttu-id="3a2e4-167">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-168">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-169">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="3a2e4-170">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3a2e4-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a2e4-171">Az.ApiManagement</span></span>
* <span data-ttu-id="3a2e4-172">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="3a2e4-173">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="3a2e4-174">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-175">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-176">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="3a2e4-177">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="3a2e4-178">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-179">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-180">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="3a2e4-181">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3a2e4-182">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="3a2e4-183">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="3a2e4-184">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="3a2e4-185">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="3a2e4-186">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="3a2e4-187">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="3a2e4-188">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-189">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-190">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="3a2e4-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="3a2e4-191">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3a2e4-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a2e4-192">Az.HDInsight</span></span>
* <span data-ttu-id="3a2e4-193">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a2e4-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-194">Az.IotHub</span></span>
* <span data-ttu-id="3a2e4-195">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="3a2e4-196">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="3a2e4-197">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-197">New cmdlets are:</span></span>
    - <span data-ttu-id="3a2e4-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a2e4-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3a2e4-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a2e4-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3a2e4-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a2e4-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3a2e4-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a2e4-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a2e4-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-202">Az.Monitor</span></span>
* <span data-ttu-id="3a2e4-203">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="3a2e4-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="3a2e4-204">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="3a2e4-205">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="3a2e4-206">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="3a2e4-207">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="3a2e4-208">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="3a2e4-209">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="3a2e4-210">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="3a2e4-211">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3a2e4-212">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="3a2e4-213">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3a2e4-214">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="3a2e4-215">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="3a2e4-216">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="3a2e4-217">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a2e4-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="3a2e4-218">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="3a2e4-219">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a2e4-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="3a2e4-220">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="3a2e4-221">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="3a2e4-222">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-222">Overall improved help files</span></span>
* <span data-ttu-id="3a2e4-223">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-224">Az.Network</span></span>
* <span data-ttu-id="3a2e4-225">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="3a2e4-226">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="3a2e4-227">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="3a2e4-228">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="3a2e4-229">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="3a2e4-230">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="3a2e4-231">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="3a2e4-232">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="3a2e4-233">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="3a2e4-234">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="3a2e4-235">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="3a2e4-236">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="3a2e4-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="3a2e4-237">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-237">New cmdlets</span></span>
        - <span data-ttu-id="3a2e4-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3a2e4-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="3a2e4-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="3a2e4-240">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="3a2e4-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3a2e4-241">New-VpnSite</span></span>
        - <span data-ttu-id="3a2e4-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3a2e4-242">Update-VpnSite</span></span>
        - <span data-ttu-id="3a2e4-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-243">New-VpnConnection</span></span>
        - <span data-ttu-id="3a2e4-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-244">Update-VpnConnection</span></span>
* <span data-ttu-id="3a2e4-245">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-247">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="3a2e4-248">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-249">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-250">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a2e4-252">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="3a2e4-253">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="3a2e4-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a2e4-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a2e4-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3a2e4-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3a2e4-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3a2e4-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3a2e4-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3a2e4-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="3a2e4-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a2e4-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a2e4-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a2e4-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a2e4-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3a2e4-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3a2e4-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3a2e4-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3a2e4-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3a2e4-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="3a2e4-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a2e4-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a2e4-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3a2e4-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3a2e4-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3a2e4-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3a2e4-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="3a2e4-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="3a2e4-267">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a2e4-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a2e4-268">Az.SignalR</span></span>
* <span data-ttu-id="3a2e4-269">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-270">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-271">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="3a2e4-272">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="3a2e4-273">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3a2e4-274">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="3a2e4-275">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-276">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-277">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="3a2e4-278">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="3a2e4-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="3a2e4-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="3a2e4-281">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="3a2e4-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="3a2e4-283">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="3a2e4-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a2e4-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3a2e4-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a2e4-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3a2e4-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a2e4-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3a2e4-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a2e4-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-288">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-289">Uygulama yeni ASP’ye geçirilirken webapp etiketlerinin silinmesine neden olan sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="3a2e4-290">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="3a2e4-291">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="3a2e4-292">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="3a2e4-293">Genel</span><span class="sxs-lookup"><span data-stu-id="3a2e4-293">General</span></span>
* <span data-ttu-id="3a2e4-294">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-295">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-296">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="3a2e4-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3a2e4-297">Az.Aks</span></span>
* <span data-ttu-id="3a2e4-298">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="3a2e4-299">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="3a2e4-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3a2e4-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a2e4-300">Az.ApiManagement</span></span>
* <span data-ttu-id="3a2e4-301">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="3a2e4-302">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="3a2e4-303">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="3a2e4-304">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="3a2e4-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="3a2e4-305">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3a2e4-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a2e4-306">Az.Batch</span></span>
* <span data-ttu-id="3a2e4-307">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a2e4-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a2e4-308">Az.Cdn</span></span>
* <span data-ttu-id="3a2e4-309">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-310">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-311">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="3a2e4-312">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="3a2e4-313">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="3a2e4-314">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="3a2e4-315">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="3a2e4-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="3a2e4-316">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="3a2e4-317">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="3a2e4-318">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-319">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-320">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="3a2e4-321">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="3a2e4-322">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="3a2e4-323">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-325">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a2e4-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-326">Az.EventHub</span></span>
* <span data-ttu-id="3a2e4-327">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="3a2e4-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="3a2e4-328">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="3a2e4-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="3a2e4-329">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="3a2e4-330">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="3a2e4-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="3a2e4-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3a2e4-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3a2e4-332">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a2e4-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-333">Az.Monitor</span></span>
* <span data-ttu-id="3a2e4-334">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-335">Az.Network</span></span>
* <span data-ttu-id="3a2e4-336">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="3a2e4-337">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="3a2e4-338">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="3a2e4-339">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="3a2e4-340">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="3a2e4-341">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="3a2e4-342">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a2e4-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a2e4-344">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="3a2e4-345">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-345">Added example</span></span>
    - <span data-ttu-id="3a2e4-346">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="3a2e4-347">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="3a2e4-348">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-350">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-351">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-352">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="3a2e4-353">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="3a2e4-354">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="3a2e4-355">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a2e4-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a2e4-356">Az.ServiceBus</span></span>
* <span data-ttu-id="3a2e4-357">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="3a2e4-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="3a2e4-358">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="3a2e4-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="3a2e4-359">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a2e4-361">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="3a2e4-362">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="3a2e4-363">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="3a2e4-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="3a2e4-364">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="3a2e4-365">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="3a2e4-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="3a2e4-366">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-367">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-368">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-369">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-370">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="3a2e4-371">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="3a2e4-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="3a2e4-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="3a2e4-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="3a2e4-374">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="3a2e4-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="3a2e4-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-376">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-377">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="3a2e4-378">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-379">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-380">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="3a2e4-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="3a2e4-382">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-383">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-384">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a2e4-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a2e4-386">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-387">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-388">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3a2e4-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3a2e4-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3a2e4-390">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="3a2e4-391">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="3a2e4-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-392">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-393">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="3a2e4-394">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a2e4-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-395">Az.EventHub</span></span>
* <span data-ttu-id="3a2e4-396">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3a2e4-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3a2e4-397">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a2e4-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a2e4-398">Az.KeyVault</span></span>
* <span data-ttu-id="3a2e4-399">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a2e4-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a2e4-400">Az.LogicApp</span></span>
* <span data-ttu-id="3a2e4-401">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="3a2e4-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="3a2e4-402">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="3a2e4-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-403">Az.ManagedServices</span></span>
* <span data-ttu-id="3a2e4-404">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-405">Az.Network</span></span>
* <span data-ttu-id="3a2e4-406">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="3a2e4-407">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-407">New cmdlets</span></span>
        - <span data-ttu-id="3a2e4-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a2e4-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a2e4-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a2e4-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3a2e4-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a2e4-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a2e4-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a2e4-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a2e4-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="3a2e4-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="3a2e4-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a2e4-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="3a2e4-416">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="3a2e4-417">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="3a2e4-418">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="3a2e4-419">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="3a2e4-420">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="3a2e4-421">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="3a2e4-422">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-422">Updated cmdlets</span></span>
        - <span data-ttu-id="3a2e4-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a2e4-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a2e4-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3a2e4-426">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3a2e4-427">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="3a2e4-428">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="3a2e4-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3a2e4-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3a2e4-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="3a2e4-432">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="3a2e4-433">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="3a2e4-434">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a2e4-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a2e4-436">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="3a2e4-437">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-439">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3a2e4-440">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="3a2e4-441">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="3a2e4-442">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3a2e4-443">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="3a2e4-444">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3a2e4-445">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="3a2e4-446">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3a2e4-447">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="3a2e4-448">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-449">Az.Resources</span></span>
- <span data-ttu-id="3a2e4-450">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="3a2e4-451">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a2e4-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a2e4-452">Az.ServiceBus</span></span>
* <span data-ttu-id="3a2e4-453">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3a2e4-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3a2e4-454">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-455">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-456">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="3a2e4-457">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="3a2e4-458">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-459">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-460">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3a2e4-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3a2e4-461">Az.StorageSync</span></span>
* <span data-ttu-id="3a2e4-462">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="3a2e4-463">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-464">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-465">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="3a2e4-466">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="3a2e4-467">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="3a2e4-468">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-469">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-470">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="3a2e4-471">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="3a2e4-472">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3a2e4-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-473">Az.Advisor</span></span>
* <span data-ttu-id="3a2e4-474">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="3a2e4-475">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3a2e4-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a2e4-476">Az.ApiManagement</span></span>
* <span data-ttu-id="3a2e4-477">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="3a2e4-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="3a2e4-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="3a2e4-479">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="3a2e4-480">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="3a2e4-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="3a2e4-481">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="3a2e4-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="3a2e4-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3a2e4-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="3a2e4-483">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-484">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-485">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-486">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-487">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-488">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-489">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a2e4-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a2e4-490">Az.EventGrid</span></span>
* <span data-ttu-id="3a2e4-491">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a2e4-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-492">Az.IotHub</span></span>
* <span data-ttu-id="3a2e4-493">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-494">Az.Network</span></span>
* <span data-ttu-id="3a2e4-495">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="3a2e4-496">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a2e4-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a2e4-498">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="3a2e4-499">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="3a2e4-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a2e4-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a2e4-501">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-503">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-504">Az.Resources</span></span>
    - <span data-ttu-id="3a2e4-505">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="3a2e4-506">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="3a2e4-507">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="3a2e4-508">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a2e4-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a2e4-509">Az.ServiceBus</span></span>
* <span data-ttu-id="3a2e4-510">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-511">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-512">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="3a2e4-513">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="3a2e4-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3a2e4-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3a2e4-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3a2e4-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3a2e4-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3a2e4-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3a2e4-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3a2e4-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3a2e4-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3a2e4-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3a2e4-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3a2e4-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="3a2e4-520">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-521">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-522">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="3a2e4-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a2e4-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="3a2e4-524">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="3a2e4-525">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="3a2e4-526">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="3a2e4-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3a2e4-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3a2e4-529">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="3a2e4-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3a2e4-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="3a2e4-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3a2e4-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3a2e4-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3a2e4-532">Az.StorageSync</span></span>
* <span data-ttu-id="3a2e4-533">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="3a2e4-534">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-535">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-536">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="3a2e4-537">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="3a2e4-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="3a2e4-538">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="3a2e4-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3a2e4-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="3a2e4-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="3a2e4-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-541">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-542">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="3a2e4-543">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="3a2e4-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3a2e4-544">Az.Dns</span></span>
* <span data-ttu-id="3a2e4-545">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a2e4-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a2e4-546">Az.EventGrid</span></span>
* <span data-ttu-id="3a2e4-547">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="3a2e4-548">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-548">New cmdlets:</span></span>
    - <span data-ttu-id="3a2e4-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3a2e4-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3a2e4-550">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3a2e4-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3a2e4-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3a2e4-552">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="3a2e4-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3a2e4-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3a2e4-554">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3a2e4-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3a2e4-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3a2e4-556">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3a2e4-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3a2e4-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3a2e4-558">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="3a2e4-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3a2e4-560">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="3a2e4-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3a2e4-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="3a2e4-562">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="3a2e4-563">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3a2e4-564">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="3a2e4-565">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="3a2e4-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="3a2e4-567">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3a2e4-568">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3a2e4-569">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="3a2e4-570">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="3a2e4-571">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="3a2e4-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="3a2e4-572">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="3a2e4-573">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="3a2e4-574">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="3a2e4-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="3a2e4-576">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="3a2e4-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3a2e4-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="3a2e4-578">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="3a2e4-579">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3a2e4-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-580">Az.FrontDoor</span></span>
* <span data-ttu-id="3a2e4-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="3a2e4-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="3a2e4-582">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="3a2e4-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3a2e4-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="3a2e4-584">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-585">Az.Network</span></span>
* <span data-ttu-id="3a2e4-586">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="3a2e4-587">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-587">New cmdlets</span></span>
        - <span data-ttu-id="3a2e4-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3a2e4-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="3a2e4-589">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="3a2e4-590">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-590">New cmdlets</span></span> 
        - <span data-ttu-id="3a2e4-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="3a2e4-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="3a2e4-592">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="3a2e4-593">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-593">New cmdlets</span></span> 
        - <span data-ttu-id="3a2e4-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a2e4-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="3a2e4-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a2e4-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3a2e4-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a2e4-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3a2e4-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="3a2e4-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3a2e4-599">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="3a2e4-600">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-600">New cmdlets</span></span>
        - <span data-ttu-id="3a2e4-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a2e4-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a2e4-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a2e4-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a2e4-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a2e4-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a2e4-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="3a2e4-605">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="3a2e4-606">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="3a2e4-607">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="3a2e4-608">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="3a2e4-609">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="3a2e4-610">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="3a2e4-611">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="3a2e4-612">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="3a2e4-613">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="3a2e4-614">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="3a2e4-615">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="3a2e4-616">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="3a2e4-617">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="3a2e4-618">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="3a2e4-619">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="3a2e4-620">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="3a2e4-621">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="3a2e4-622">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a2e4-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="3a2e4-623">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3a2e4-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="3a2e4-624">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="3a2e4-625">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3a2e4-626">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3a2e4-627">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a2e4-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a2e4-629">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-630">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-631">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="3a2e4-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="3a2e4-632">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3a2e4-633">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3a2e4-634">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a2e4-636">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-637">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-638">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="3a2e4-639">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="3a2e4-640">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="3a2e4-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a2e4-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3a2e4-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a2e4-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3a2e4-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a2e4-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3a2e4-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3a2e4-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="3a2e4-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3a2e4-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-646">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-647">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="3a2e4-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="3a2e4-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="3a2e4-649">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="3a2e4-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-651">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-652">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="3a2e4-653">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="3a2e4-654">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="3a2e4-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a2e4-655">Az.Cdn</span></span>
* <span data-ttu-id="3a2e4-656">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-657">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-658">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="3a2e4-659">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a2e4-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a2e4-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-660">Az.EventHub</span></span>
* <span data-ttu-id="3a2e4-661">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="3a2e4-662">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-663">Az.Network</span></span>
* <span data-ttu-id="3a2e4-664">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="3a2e4-665">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a2e4-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a2e4-667">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-669">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a2e4-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a2e4-670">Az.ServiceBus</span></span>
* <span data-ttu-id="3a2e4-671">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a2e4-673">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="3a2e4-674">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-675">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-676">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="3a2e4-677">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3a2e4-678">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="3a2e4-679">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-680">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-681">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="3a2e4-682">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3a2e4-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a2e4-683">Az.ApiManagement</span></span>
* <span data-ttu-id="3a2e4-684">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="3a2e4-685">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="3a2e4-686">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="3a2e4-687">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="3a2e4-688">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="3a2e4-689">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="3a2e4-690">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="3a2e4-691">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="3a2e4-692">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="3a2e4-693">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="3a2e4-694">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="3a2e4-695">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="3a2e4-696">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="3a2e4-697">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="3a2e4-698">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="3a2e4-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="3a2e4-699">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="3a2e4-700">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="3a2e4-701">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="3a2e4-702">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="3a2e4-703">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="3a2e4-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="3a2e4-704">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="3a2e4-705">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="3a2e4-706">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="3a2e4-707">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="3a2e4-708">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="3a2e4-709">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="3a2e4-710">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="3a2e4-711">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="3a2e4-712">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="3a2e4-713">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="3a2e4-714">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="3a2e4-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="3a2e4-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="3a2e4-716">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="3a2e4-717">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3a2e4-718">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="3a2e4-719">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="3a2e4-720">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="3a2e4-721">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="3a2e4-722">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="3a2e4-723">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="3a2e4-724">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3a2e4-725">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3a2e4-726">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="3a2e4-727">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3a2e4-728">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3a2e4-729">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3a2e4-730">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="3a2e4-731">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3a2e4-732">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="3a2e4-733">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="3a2e4-734">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="3a2e4-735">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="3a2e4-736">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="3a2e4-737">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="3a2e4-738">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="3a2e4-739">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="3a2e4-740">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3a2e4-741">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3a2e4-742">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3a2e4-743">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3a2e4-744">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3a2e4-745">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3a2e4-746">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3a2e4-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3a2e4-747">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3a2e4-748">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="3a2e4-749">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="3a2e4-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="3a2e4-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="3a2e4-751">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="3a2e4-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="3a2e4-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="3a2e4-753">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="3a2e4-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="3a2e4-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="3a2e4-755">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="3a2e4-756">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="3a2e4-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="3a2e4-758">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="3a2e4-759">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="3a2e4-760">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="3a2e4-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-761">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-762">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="3a2e4-763">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="3a2e4-764">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="3a2e4-765">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="3a2e4-766">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="3a2e4-767">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="3a2e4-768">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-769">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-770">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="3a2e4-771">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-773">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a2e4-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-774">Az.Monitor</span></span>
* <span data-ttu-id="3a2e4-775">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-776">Az.Network</span></span>
* <span data-ttu-id="3a2e4-777">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="3a2e4-778">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="3a2e4-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a2e4-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="3a2e4-780">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-781">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-782">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-783">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-784">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="3a2e4-785">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-786">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-787">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="3a2e4-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a2e4-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a2e4-789">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="3a2e4-790">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-791">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-792">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="3a2e4-793">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3a2e4-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="3a2e4-794">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="3a2e4-795">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="3a2e4-796">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="3a2e4-797">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="3a2e4-798">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-798">Breaking changes</span></span>
    - <span data-ttu-id="3a2e4-799">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="3a2e4-800">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3a2e4-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3a2e4-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="3a2e4-802">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="3a2e4-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3a2e4-803">Az.Dns</span></span>
* <span data-ttu-id="3a2e4-804">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="3a2e4-805">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="3a2e4-806">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3a2e4-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-807">Az.FrontDoor</span></span>
* <span data-ttu-id="3a2e4-808">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="3a2e4-809">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="3a2e4-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="3a2e4-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a2e4-810">Az.HDInsight</span></span>
* <span data-ttu-id="3a2e4-811">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="3a2e4-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3a2e4-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="3a2e4-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3a2e4-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3a2e4-814">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3a2e4-815">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="3a2e4-816">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="3a2e4-817">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a2e4-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-818">Az.Monitor</span></span>
* <span data-ttu-id="3a2e4-819">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="3a2e4-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3a2e4-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="3a2e4-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a2e4-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="3a2e4-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="3a2e4-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="3a2e4-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="3a2e4-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="3a2e4-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="3a2e4-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="3a2e4-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="3a2e4-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a2e4-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a2e4-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a2e4-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a2e4-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a2e4-831">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="3a2e4-832">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-833">Az.Network</span></span>
* <span data-ttu-id="3a2e4-834">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="3a2e4-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="3a2e4-835">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-835">New cmdlets</span></span>
        - <span data-ttu-id="3a2e4-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a2e4-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="3a2e4-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a2e4-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="3a2e4-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a2e4-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="3a2e4-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a2e4-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="3a2e4-840">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-840">Updated cmdlets</span></span>
        - <span data-ttu-id="3a2e4-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3a2e4-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="3a2e4-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3a2e4-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="3a2e4-843">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="3a2e4-844">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="3a2e4-845">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a2e4-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a2e4-847">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="3a2e4-848">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="3a2e4-849">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-851">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="3a2e4-852">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="3a2e4-853">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="3a2e4-854">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="3a2e4-855">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="3a2e4-856">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="3a2e4-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3a2e4-857">Az.Relay</span></span>
* <span data-ttu-id="3a2e4-858">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="3a2e4-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a2e4-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a2e4-859">Az.ServiceBus</span></span>
* <span data-ttu-id="3a2e4-860">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-861">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-862">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="3a2e4-863">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="3a2e4-864">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="3a2e4-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="3a2e4-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="3a2e4-866">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="3a2e4-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="3a2e4-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="3a2e4-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="3a2e4-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-870">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-871">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="3a2e4-872">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="3a2e4-873">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a2e4-874">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="3a2e4-874">Highlights since the last major release</span></span>
* <span data-ttu-id="3a2e4-875">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-875">General availability of `Az` module</span></span>
* <span data-ttu-id="3a2e4-876">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a2e4-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a2e4-877">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a2e4-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a2e4-878">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a2e4-879">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a2e4-880">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a2e4-881">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-882">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-883">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3a2e4-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a2e4-884">Az.Batch</span></span>
* <span data-ttu-id="3a2e4-885">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a2e4-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a2e4-886">Az.Cdn</span></span>
* <span data-ttu-id="3a2e4-887">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a2e4-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a2e4-889">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-890">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-891">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="3a2e4-892">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a2e4-893">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-894">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-895">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-897">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a2e4-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a2e4-898">Az.EventGrid</span></span>
* <span data-ttu-id="3a2e4-899">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a2e4-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-900">Az.EventHub</span></span>
* <span data-ttu-id="3a2e4-901">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="3a2e4-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a2e4-902">Az.HDInsight</span></span>
* <span data-ttu-id="3a2e4-903">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a2e4-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-904">Az.IotHub</span></span>
* <span data-ttu-id="3a2e4-905">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a2e4-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a2e4-906">Az.KeyVault</span></span>
* <span data-ttu-id="3a2e4-907">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a2e4-908">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3a2e4-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3a2e4-909">Az.MachineLearning</span></span>
* <span data-ttu-id="3a2e4-910">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="3a2e4-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3a2e4-911">Az.Media</span></span>
* <span data-ttu-id="3a2e4-912">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a2e4-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-913">Az.Monitor</span></span>
  * <span data-ttu-id="3a2e4-914">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="3a2e4-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3a2e4-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="3a2e4-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="3a2e4-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="3a2e4-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a2e4-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3a2e4-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a2e4-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3a2e4-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a2e4-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="3a2e4-920">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-921">Az.Network</span></span>
* <span data-ttu-id="3a2e4-922">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a2e4-923">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="3a2e4-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3a2e4-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="3a2e4-925">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a2e4-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a2e4-927">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3a2e4-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3a2e4-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3a2e4-929">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-931">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a2e4-932">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="3a2e4-933">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="3a2e4-934">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a2e4-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a2e4-935">Az.RedisCache</span></span>
* <span data-ttu-id="3a2e4-936">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-937">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-938">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-939">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-940">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="3a2e4-941">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a2e4-942">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="3a2e4-943">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="3a2e4-944">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="3a2e4-945">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="3a2e4-946">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-947">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-948">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="3a2e4-949">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a2e4-950">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="3a2e4-951">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="3a2e4-952">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a2e4-953">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="3a2e4-953">Highlights since the last major release</span></span>
* <span data-ttu-id="3a2e4-954">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-954">General availability of `Az` module</span></span>
* <span data-ttu-id="3a2e4-955">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a2e4-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a2e4-956">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a2e4-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a2e4-957">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a2e4-958">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a2e4-959">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a2e4-960">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-961">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-962">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a2e4-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a2e4-964">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3a2e4-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="3a2e4-965">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="3a2e4-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-966">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-967">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="3a2e4-968">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="3a2e4-969">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-970">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-971">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3a2e4-972">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="3a2e4-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a2e4-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="3a2e4-974">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-975">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-976">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="3a2e4-977">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-978">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-979">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="3a2e4-980">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3a2e4-981">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="3a2e4-982">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3a2e4-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="3a2e4-983">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="3a2e4-984">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3a2e4-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-985">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-986">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-987">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-988">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="3a2e4-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="3a2e4-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a2e4-989">New-AzStorageContext</span></span>
* <span data-ttu-id="3a2e4-990">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="3a2e4-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="3a2e4-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3a2e4-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3a2e4-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3a2e4-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3a2e4-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="3a2e4-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="3a2e4-995">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="3a2e4-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="3a2e4-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3a2e4-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3a2e4-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="3a2e4-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a2e4-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="3a2e4-1000">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a2e4-1001">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="3a2e4-1002">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="3a2e4-1003">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a2e4-1004">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a2e4-1005">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a2e4-1006">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a2e4-1007">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a2e4-1008">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1009">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-1010">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="3a2e4-1011">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="3a2e4-1012">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1012">Pre-Post script</span></span>
    * <span data-ttu-id="3a2e4-1013">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1014">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1015">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="3a2e4-1016">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a2e4-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1017">Az.KeyVault</span></span>
* <span data-ttu-id="3a2e4-1018">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1019">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1020">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="3a2e4-1021">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-1023">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="3a2e4-1024">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1025">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1026">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="3a2e4-1027">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1028">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1029">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1030">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-1031">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="3a2e4-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a2e4-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a2e4-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a2e4-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="3a2e4-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="3a2e4-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1038">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-1039">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="3a2e4-1040">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1041">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-1042">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="3a2e4-1043">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1044">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-1045">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="3a2e4-1046">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="3a2e4-1047">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a2e4-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1048">Az.Cdn</span></span>
* <span data-ttu-id="3a2e4-1049">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1050">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1051">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1052">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-1053">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a2e4-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1054">Az.LogicApp</span></span>
* <span data-ttu-id="3a2e4-1055">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1056">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1057">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-1059">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="3a2e4-1060">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1060">SDK Update</span></span>
* <span data-ttu-id="3a2e4-1061">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="3a2e4-1062">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1063">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1064">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="3a2e4-1065">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="3a2e4-1066">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="3a2e4-1067">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="3a2e4-1068">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="3a2e4-1069">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1070">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1071">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="3a2e4-1072">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1073">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-1074">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="3a2e4-1075">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="3a2e4-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a2e4-1077">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1078">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-1079">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="3a2e4-1080">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="3a2e4-1081">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a2e4-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a2e4-1083">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1084">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1085">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="3a2e4-1086">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="3a2e4-1087">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="3a2e4-1088">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-1090">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a2e4-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1091">Az.EventHub</span></span>
* <span data-ttu-id="3a2e4-1092">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="3a2e4-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1093">Az.KeyVault</span></span>
* <span data-ttu-id="3a2e4-1094">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a2e4-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1095">Az.LogicApp</span></span>
* <span data-ttu-id="3a2e4-1096">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="3a2e4-1097">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="3a2e4-1098">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="3a2e4-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a2e4-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a2e4-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a2e4-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="3a2e4-1103">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="3a2e4-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a2e4-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a2e4-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a2e4-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="3a2e4-1108">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a2e4-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1109">Az.Monitor</span></span>
* <span data-ttu-id="3a2e4-1110">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1111">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1112">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a2e4-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a2e4-1114">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="3a2e4-1115">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="3a2e4-1116">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1117">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1118">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3a2e4-1119">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="3a2e4-1120">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="3a2e4-1121">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1122">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1123">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="3a2e4-1124">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1125">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-1126">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="3a2e4-1127">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1128">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-1129">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a2e4-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="3a2e4-1131">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1132">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1133">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="3a2e4-1134">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="3a2e4-1135">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="3a2e4-1137">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1138">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1139">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="3a2e4-1140">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3a2e4-1141">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="3a2e4-1142">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1143">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="3a2e4-1145">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="3a2e4-1146">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="3a2e4-1147">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1148">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-1149">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a2e4-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a2e4-1151">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a2e4-1153">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="3a2e4-1154">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1155">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-1156">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a2e4-1157">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a2e4-1158">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="3a2e4-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1159">Az.Aks</span></span>
* <span data-ttu-id="3a2e4-1160">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a2e4-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1161">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-1162">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="3a2e4-1163">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a2e4-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1164">Az.Cdn</span></span>
* <span data-ttu-id="3a2e4-1165">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1166">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1167">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="3a2e4-1168">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="3a2e4-1169">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3a2e4-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3a2e4-1171">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a2e4-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1172">Az.DataFactory</span></span>
* <span data-ttu-id="3a2e4-1173">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-1175">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="3a2e4-1176">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="3a2e4-1177">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a2e4-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1178">Az.IotHub</span></span>
* <span data-ttu-id="3a2e4-1179">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a2e4-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1180">Az.KeyVault</span></span>
* <span data-ttu-id="3a2e4-1181">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1182">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1183">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1184">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1185">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="3a2e4-1186">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="3a2e4-1187">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="3a2e4-1188">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="3a2e4-1189">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="3a2e4-1190">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="3a2e4-1191">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a2e4-1193">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="3a2e4-1194">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1194">Fix some error messages.</span></span>
* <span data-ttu-id="3a2e4-1195">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="3a2e4-1196">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a2e4-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1197">Az.SignalR</span></span>
* <span data-ttu-id="3a2e4-1198">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1199">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1200">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a2e4-1201">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="3a2e4-1202">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="3a2e4-1203">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1204">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-1205">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a2e4-1206">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="3a2e4-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="3a2e4-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3a2e4-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="3a2e4-1210">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1211">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-1212">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a2e4-1213">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="3a2e4-1214">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="3a2e4-1215">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a2e4-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1216">Az.Accounts</span></span>
* <span data-ttu-id="3a2e4-1217">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1218">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1219">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3a2e4-1220">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3a2e4-1221">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-1223">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3a2e4-1224">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a2e4-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1225">Az.EventGrid</span></span>
* <span data-ttu-id="3a2e4-1226">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3a2e4-1227">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3a2e4-1228">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3a2e4-1229">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3a2e4-1230">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3a2e4-1231">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3a2e4-1232">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3a2e4-1233">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3a2e4-1234">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3a2e4-1235">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="3a2e4-1236">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3a2e4-1237">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a2e4-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1238">Az.IotHub</span></span>
* <span data-ttu-id="3a2e4-1239">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a2e4-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1240">Az.LogicApp</span></span>
* <span data-ttu-id="3a2e4-1241">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1242">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1243">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3a2e4-1244">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3a2e4-1245">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3a2e4-1246">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3a2e4-1247">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3a2e4-1248">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a2e4-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1249">Az.SignalR</span></span>
* <span data-ttu-id="3a2e4-1250">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1251">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1252">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a2e4-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1253">Az.Storage</span></span>
* <span data-ttu-id="3a2e4-1254">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3a2e4-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="3a2e4-1256">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3a2e4-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1258">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-1259">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3a2e4-1260">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3a2e4-1261">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3a2e4-1262">Genel</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1262">General</span></span>

- <span data-ttu-id="3a2e4-1263">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="3a2e4-1264">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1264">Online help for each module</span></span>
- <span data-ttu-id="3a2e4-1265">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3a2e4-1266">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3a2e4-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1267">Az.Accounts</span></span>
- <span data-ttu-id="3a2e4-1268">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="3a2e4-1269">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3a2e4-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="3a2e4-1271">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1271">Fixes for #7002</span></span>
- <span data-ttu-id="3a2e4-1272">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3a2e4-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1273">Az.Batch</span></span>
- <span data-ttu-id="3a2e4-1274">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3a2e4-1275">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3a2e4-1276">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3a2e4-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1277">Az.Billing</span></span>
- <span data-ttu-id="3a2e4-1278">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3a2e4-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="3a2e4-1280">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3a2e4-1281">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3a2e4-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="3a2e4-1283">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3a2e4-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3a2e4-1285">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="3a2e4-1287">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3a2e4-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1288">Az.Monitor</span></span>
- <span data-ttu-id="3a2e4-1289">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3a2e4-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1290">Az.KeyVault</span></span>
- <span data-ttu-id="3a2e4-1291">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3a2e4-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="3a2e4-1293">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3a2e4-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1294">Az.Media</span></span>
- <span data-ttu-id="3a2e4-1295">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1296">Az.Network</span></span>
<span data-ttu-id="3a2e4-1297">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3a2e4-1298">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="3a2e4-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a2e4-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a2e4-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a2e4-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a2e4-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a2e4-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3a2e4-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3a2e4-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3a2e4-1307">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3a2e4-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3a2e4-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3a2e4-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3a2e4-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3a2e4-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3a2e4-1313">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3a2e4-1314">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3a2e4-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3a2e4-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3a2e4-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3a2e4-1318">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3a2e4-1319">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3a2e4-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="3a2e4-1321">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3a2e4-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1322">Az.Profile</span></span>
- <span data-ttu-id="3a2e4-1323">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="3a2e4-1325">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3a2e4-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1326">Az.Resources</span></span>
- <span data-ttu-id="3a2e4-1327">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="3a2e4-1329">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3a2e4-1330">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3a2e4-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="3a2e4-1332">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3a2e4-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1333">Az.Sql</span></span>
- <span data-ttu-id="3a2e4-1334">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3a2e4-1335">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3a2e4-1336">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3a2e4-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1337">Az.Storage</span></span>
- <span data-ttu-id="3a2e4-1338">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3a2e4-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1339">Az.Websites</span></span>
- <span data-ttu-id="3a2e4-1340">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3a2e4-1341">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3a2e4-1342">Genel</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1342">General</span></span>

* <span data-ttu-id="3a2e4-1343">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3a2e4-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1344">Az.Compute</span></span>

* <span data-ttu-id="3a2e4-1345">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="3a2e4-1347">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3a2e4-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="3a2e4-1349">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="3a2e4-1350">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3a2e4-1351">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3a2e4-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="3a2e4-1353">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3a2e4-1354">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3a2e4-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1355">Az.Resources</span></span>

* <span data-ttu-id="3a2e4-1356">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3a2e4-1357">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3a2e4-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1358">Az.Sql</span></span>

* <span data-ttu-id="3a2e4-1359">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3a2e4-1360">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3a2e4-1361">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3a2e4-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1362">Az.Storage</span></span>

* <span data-ttu-id="3a2e4-1363">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3a2e4-1364">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3a2e4-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3a2e4-1366">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="3a2e4-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3a2e4-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3a2e4-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1369">Az.Websites</span></span>

* <span data-ttu-id="3a2e4-1370">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="3a2e4-1371">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3a2e4-1372">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3a2e4-1373">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3a2e4-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="3a2e4-1375">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3a2e4-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1376">Az.Automation</span></span>
* <span data-ttu-id="3a2e4-1377">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3a2e4-1378">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3a2e4-1379">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3a2e4-1380">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3a2e4-1381">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3a2e4-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1382">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1383">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3a2e4-1384">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3a2e4-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="3a2e4-1386">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3a2e4-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3a2e4-1388">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1389">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1390">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3a2e4-1391">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3a2e4-1392">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="3a2e4-1393">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3a2e4-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3a2e4-1395">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3a2e4-1396">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3a2e4-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3a2e4-1398">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3a2e4-1399">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3a2e4-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1400">Az.Relay</span></span>
* <span data-ttu-id="3a2e4-1401">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3a2e4-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1402">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1403">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3a2e4-1404">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3a2e4-1405">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a2e4-1407">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3a2e4-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1408">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1409">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3a2e4-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a2e4-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a2e4-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a2e4-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a2e4-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a2e4-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a2e4-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a2e4-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3a2e4-1418">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3a2e4-1419">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3a2e4-1420">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3a2e4-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3a2e4-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3a2e4-1423">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3a2e4-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3a2e4-1425">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3a2e4-1426">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3a2e4-1427">Genel</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1427">General</span></span>
* <span data-ttu-id="3a2e4-1428">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3a2e4-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1429">Az.Profile</span></span>
* <span data-ttu-id="3a2e4-1430">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3a2e4-1431">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3a2e4-1432">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3a2e4-1433">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3a2e4-1434">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3a2e4-1435">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3a2e4-1436">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a2e4-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a2e4-1438">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1439">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1440">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3a2e4-1441">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3a2e4-1442">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-1444">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3a2e4-1445">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3a2e4-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1446">Az.Insights</span></span>
* <span data-ttu-id="3a2e4-1447">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3a2e4-1448">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3a2e4-1449">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3a2e4-1450">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1451">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1452">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3a2e4-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3a2e4-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3a2e4-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3a2e4-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3a2e4-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3a2e4-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a2e4-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a2e4-1460">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1461">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1462">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3a2e4-1463">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a2e4-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="3a2e4-1465">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a2e4-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a2e4-1467">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3a2e4-1468">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3a2e4-1469">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3a2e4-1470">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3a2e4-1471">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3a2e4-1472">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3a2e4-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1473">Az.Profile</span></span>
* <span data-ttu-id="3a2e4-1474">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3a2e4-1475">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1476">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1477">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3a2e4-1478">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a2e4-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a2e4-1480">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3a2e4-1481">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3a2e4-1482">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3a2e4-1483">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3a2e4-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1485">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1486">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3a2e4-1487">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1488">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1489">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3a2e4-1490">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3a2e4-1491">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3a2e4-1492">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1492">Azure.Storage</span></span>
* <span data-ttu-id="3a2e4-1493">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3a2e4-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3a2e4-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3a2e4-1496">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3a2e4-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="3a2e4-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a2e4-1499">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a2e4-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1500">Az.Compute</span></span>
* <span data-ttu-id="3a2e4-1501">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3a2e4-1502">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3a2e4-1503">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3a2e4-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3a2e4-1505">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a2e4-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1506">Az.Network</span></span>
* <span data-ttu-id="3a2e4-1507">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3a2e4-1508">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1508">new cmdlets added</span></span>
    - <span data-ttu-id="3a2e4-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a2e4-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a2e4-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a2e4-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a2e4-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3a2e4-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3a2e4-1515">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3a2e4-1516">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3a2e4-1517">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a2e4-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1518">Az.RedisCache</span></span>
* <span data-ttu-id="3a2e4-1519">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3a2e4-1520">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a2e4-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1521">Az.Resources</span></span>
* <span data-ttu-id="3a2e4-1522">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3a2e4-1523">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a2e4-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1524">Az.Sql</span></span>
* <span data-ttu-id="3a2e4-1525">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a2e4-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1526">Az.Websites</span></span>
* <span data-ttu-id="3a2e4-1527">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3a2e4-1528">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3a2e4-1529">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3a2e4-1530">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="3a2e4-1530">Initial Release</span></span>
