---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111034"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="35460-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="35460-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="35460-104">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="35460-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-105">Az.Accounts</span></span>
* <span data-ttu-id="35460-106">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="35460-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="35460-107">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="35460-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="35460-108">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="35460-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-109">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-110">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="35460-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="35460-111">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="35460-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="35460-112">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="35460-113">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="35460-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-115">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-116">Az.IotHub</span></span>
* <span data-ttu-id="35460-117">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="35460-118">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="35460-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="35460-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="35460-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="35460-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="35460-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="35460-123">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="35460-124">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="35460-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="35460-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="35460-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="35460-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="35460-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="35460-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="35460-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="35460-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="35460-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="35460-129">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="35460-130">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="35460-131">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="35460-132">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="35460-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="35460-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="35460-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="35460-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="35460-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="35460-135">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-136">Az.Monitor</span></span>
* <span data-ttu-id="35460-137">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="35460-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-138">Az.Network</span></span>
* <span data-ttu-id="35460-139">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="35460-140">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="35460-141">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="35460-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="35460-142">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-143">Az.Resources</span></span>
* <span data-ttu-id="35460-144">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="35460-145">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="35460-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="35460-146">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="35460-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="35460-147">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="35460-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="35460-148">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="35460-149">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="35460-150">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="35460-151">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="35460-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="35460-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="35460-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="35460-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="35460-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="35460-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="35460-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="35460-155">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="35460-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="35460-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="35460-157">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="35460-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-158">Az.Sql</span></span>
* <span data-ttu-id="35460-159">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="35460-160">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="35460-161">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="35460-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="35460-162">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="35460-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="35460-163">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="35460-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="35460-164">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="35460-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="35460-165">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="35460-166">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="35460-167">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-168">Az.Storage</span></span>
* <span data-ttu-id="35460-169">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="35460-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="35460-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="35460-171">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="35460-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="35460-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="35460-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="35460-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-174">Az.Websites</span></span>
* <span data-ttu-id="35460-175">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="35460-176">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="35460-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="35460-177">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="35460-178">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="35460-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="35460-179">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="35460-180">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="35460-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35460-181">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="35460-181">Highlights since the last major release</span></span>
* <span data-ttu-id="35460-182">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="35460-183">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="35460-184">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-185">Az.Accounts</span></span>
* <span data-ttu-id="35460-186">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-187">Az.Automation</span></span>
* <span data-ttu-id="35460-188">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35460-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35460-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="35460-190">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="35460-191">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-192">Az.Compute</span></span>
* <span data-ttu-id="35460-193">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="35460-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35460-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35460-194">Az.FrontDoor</span></span>
* <span data-ttu-id="35460-195">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-196">Az.IotHub</span></span>
* <span data-ttu-id="35460-197">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="35460-198">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="35460-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="35460-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="35460-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="35460-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="35460-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="35460-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-203">Az.KeyVault</span></span>
* <span data-ttu-id="35460-204">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-205">Az.Monitor</span></span>
* <span data-ttu-id="35460-206">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="35460-207">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="35460-208">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="35460-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-209">Az.Network</span></span>
* <span data-ttu-id="35460-210">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="35460-211">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="35460-212">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="35460-213">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="35460-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="35460-214">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="35460-214">No new cmdlets are added.</span></span> <span data-ttu-id="35460-215">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="35460-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-217">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-218">Az.Resources</span></span>
* <span data-ttu-id="35460-219">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="35460-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="35460-220">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35460-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="35460-221">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35460-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="35460-222">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="35460-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="35460-223">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="35460-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="35460-224">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="35460-225">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="35460-226">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="35460-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-227">Az.Sql</span></span>
* <span data-ttu-id="35460-228">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="35460-229">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="35460-230">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="35460-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="35460-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="35460-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="35460-232">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="35460-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="35460-233">Az.StorageSync</span></span>
* <span data-ttu-id="35460-234">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="35460-235">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="35460-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35460-236">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="35460-236">Highlights since the last major release</span></span>
* <span data-ttu-id="35460-237">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="35460-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="35460-238">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-239">Az.Accounts</span></span>
* <span data-ttu-id="35460-240">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="35460-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="35460-241">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="35460-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-242">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-243">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="35460-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="35460-244">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="35460-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="35460-245">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="35460-246">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-247">Az.Compute</span></span>
* <span data-ttu-id="35460-248">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="35460-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="35460-249">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="35460-250">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="35460-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="35460-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="35460-252">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-253">Az.DataFactory</span></span>
* <span data-ttu-id="35460-254">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="35460-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="35460-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="35460-256">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="35460-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="35460-257">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="35460-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="35460-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35460-258">Az.HDInsight</span></span>
* <span data-ttu-id="35460-259">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-260">Az.KeyVault</span></span>
* <span data-ttu-id="35460-261">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-262">Az.Network</span></span>
* <span data-ttu-id="35460-263">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="35460-264">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="35460-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="35460-265">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="35460-266">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="35460-267">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="35460-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="35460-268">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="35460-269">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="35460-270">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="35460-271">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-271">New cmdlets added:</span></span>
        - <span data-ttu-id="35460-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="35460-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="35460-273">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="35460-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="35460-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="35460-275">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35460-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35460-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="35460-277">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="35460-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="35460-278">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="35460-279">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="35460-280">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-282">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="35460-283">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="35460-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-284">Az.Resources</span></span>
* <span data-ttu-id="35460-285">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="35460-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="35460-286">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-287">Az.Sql</span></span>
<span data-ttu-id="35460-288">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-289">Az.Storage</span></span>
* <span data-ttu-id="35460-290">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="35460-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="35460-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="35460-292">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="35460-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="35460-293">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-294">Az.Websites</span></span>
* <span data-ttu-id="35460-295">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="35460-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="35460-296">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="35460-297">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="35460-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-298">Az.Accounts</span></span>
* <span data-ttu-id="35460-299">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35460-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35460-300">Az.Cdn</span></span>
* <span data-ttu-id="35460-301">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="35460-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-302">Az.Compute</span></span>
* <span data-ttu-id="35460-303">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="35460-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="35460-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="35460-305">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="35460-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="35460-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="35460-307">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="35460-308">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="35460-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="35460-309">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="35460-310">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="35460-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="35460-311">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="35460-312">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="35460-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="35460-313">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="35460-314">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="35460-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="35460-315">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="35460-316">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="35460-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="35460-317">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="35460-318">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="35460-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="35460-319">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="35460-320">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="35460-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="35460-321">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="35460-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="35460-322">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="35460-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="35460-323">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="35460-324">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="35460-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-325">Az.DataFactory</span></span>
* <span data-ttu-id="35460-326">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="35460-327">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="35460-328">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="35460-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="35460-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="35460-330">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35460-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35460-331">Az.EventHub</span></span>
* <span data-ttu-id="35460-332">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="35460-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35460-333">Az.HDInsight</span></span>
* <span data-ttu-id="35460-334">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="35460-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="35460-335">Az.MachineLearning</span></span>
* <span data-ttu-id="35460-336">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="35460-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="35460-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="35460-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="35460-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="35460-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="35460-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="35460-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="35460-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="35460-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="35460-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="35460-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="35460-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="35460-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="35460-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-344">Az.Network</span></span>
* <span data-ttu-id="35460-345">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="35460-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-347">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="35460-348">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="35460-349">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="35460-350">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-351">Az.Resources</span></span>
* <span data-ttu-id="35460-352">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-353">Az.Sql</span></span>
* <span data-ttu-id="35460-354">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="35460-355">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="35460-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="35460-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="35460-357">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-358">Az.Storage</span></span>
* <span data-ttu-id="35460-359">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="35460-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="35460-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="35460-361">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="35460-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="35460-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="35460-363">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="35460-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="35460-364">Genel</span><span class="sxs-lookup"><span data-stu-id="35460-364">General</span></span>
* <span data-ttu-id="35460-365">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-366">Az.Accounts</span></span>
* <span data-ttu-id="35460-367">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="35460-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="35460-368">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="35460-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="35460-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35460-369">Az.Batch</span></span>
* <span data-ttu-id="35460-370">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-371">Az.DataFactory</span></span>
* <span data-ttu-id="35460-372">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35460-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35460-373">Az.FrontDoor</span></span>
* <span data-ttu-id="35460-374">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="35460-375">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="35460-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="35460-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="35460-377">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="35460-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-378">Az.KeyVault</span></span>
* <span data-ttu-id="35460-379">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="35460-380">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="35460-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="35460-381">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-382">Az.Monitor</span></span>
* <span data-ttu-id="35460-383">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="35460-384">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="35460-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="35460-385">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="35460-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-386">Az.Network</span></span>
* <span data-ttu-id="35460-387">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-388">Az.Resources</span></span>
* <span data-ttu-id="35460-389">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="35460-390">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-391">Az.Sql</span></span>
* <span data-ttu-id="35460-392">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="35460-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-393">Az.Storage</span></span>
* <span data-ttu-id="35460-394">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="35460-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="35460-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="35460-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="35460-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="35460-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="35460-397">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="35460-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="35460-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="35460-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="35460-399">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="35460-400">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="35460-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="35460-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="35460-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="35460-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="35460-403">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="35460-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="35460-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="35460-405">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="35460-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="35460-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="35460-407">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="35460-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35460-408">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="35460-408">Highlights since the last major release</span></span>
* <span data-ttu-id="35460-409">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="35460-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="35460-410">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="35460-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-411">Az.Compute</span></span>
* <span data-ttu-id="35460-412">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="35460-412">VM Reapply feature</span></span>
    - <span data-ttu-id="35460-413">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="35460-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="35460-414">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="35460-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="35460-415">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35460-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="35460-416">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="35460-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="35460-417">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="35460-418">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="35460-419">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="35460-420">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="35460-421">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="35460-422">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="35460-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="35460-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="35460-424">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="35460-425">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="35460-425">Get the Order</span></span>
* <span data-ttu-id="35460-426">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="35460-427">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="35460-427">Create new Order</span></span>
* <span data-ttu-id="35460-428">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="35460-429">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="35460-429">Remove the Order</span></span>
* <span data-ttu-id="35460-430">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="35460-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="35460-431">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="35460-431">Now creates Local Share</span></span>
* <span data-ttu-id="35460-432">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="35460-433">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="35460-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="35460-434">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="35460-435">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="35460-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="35460-436">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="35460-437">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="35460-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="35460-438">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="35460-439">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="35460-439">Create new Triggers</span></span>
* <span data-ttu-id="35460-440">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="35460-441">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="35460-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-442">Az.DataFactory</span></span>
* <span data-ttu-id="35460-443">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="35460-444">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-446">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35460-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35460-447">Az.EventHub</span></span>
* <span data-ttu-id="35460-448">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35460-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35460-449">Az.FrontDoor</span></span>
* <span data-ttu-id="35460-450">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="35460-451">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="35460-452">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="35460-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="35460-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-454">Az.Network</span></span>
* <span data-ttu-id="35460-455">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="35460-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="35460-456">Az.PrivateDns</span></span>
* <span data-ttu-id="35460-457">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-459">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="35460-460">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="35460-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="35460-461">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="35460-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="35460-462">Az.RedisCache</span></span>
* <span data-ttu-id="35460-463">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="35460-464">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="35460-465">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-466">Az.Resources</span></span>
- <span data-ttu-id="35460-467">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="35460-468">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="35460-469">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="35460-470">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="35460-471">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-472">Az.Sql</span></span>
* <span data-ttu-id="35460-473">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="35460-474">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="35460-475">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="35460-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="35460-476">Genel</span><span class="sxs-lookup"><span data-stu-id="35460-476">General</span></span>
* <span data-ttu-id="35460-477">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="35460-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-478">Az.Accounts</span></span>
* <span data-ttu-id="35460-479">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="35460-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="35460-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="35460-480">Az.Advisor</span></span>
* <span data-ttu-id="35460-481">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="35460-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35460-482">Az.Batch</span></span>
* <span data-ttu-id="35460-483">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="35460-484">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="35460-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="35460-485">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="35460-486">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="35460-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="35460-487">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="35460-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="35460-488">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="35460-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="35460-489">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="35460-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="35460-490">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="35460-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="35460-491">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="35460-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="35460-492">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="35460-493">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="35460-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="35460-494">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="35460-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="35460-495">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="35460-496">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="35460-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="35460-497">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="35460-498">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="35460-499">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="35460-500">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="35460-501">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="35460-502">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="35460-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="35460-503">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="35460-504">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="35460-505">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="35460-506">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="35460-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="35460-507">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="35460-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="35460-508">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="35460-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="35460-509">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="35460-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="35460-510">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="35460-511">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="35460-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="35460-512">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="35460-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="35460-513">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="35460-514">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="35460-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="35460-515">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="35460-516">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="35460-517">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="35460-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="35460-518">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="35460-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35460-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35460-519">Az.Cdn</span></span>
* <span data-ttu-id="35460-520">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="35460-521">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-522">Az.Compute</span></span>
* <span data-ttu-id="35460-523">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="35460-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="35460-524">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="35460-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="35460-525">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="35460-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="35460-526">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="35460-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="35460-527">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="35460-528">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="35460-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="35460-529">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="35460-530">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="35460-530">Breaking changes</span></span>
    - <span data-ttu-id="35460-531">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="35460-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="35460-532">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="35460-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-533">Az.DataFactory</span></span>
* <span data-ttu-id="35460-534">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-536">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="35460-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="35460-537">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="35460-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="35460-538">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="35460-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="35460-539">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="35460-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="35460-540">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="35460-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="35460-541">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="35460-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35460-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35460-542">Az.FrontDoor</span></span>
* <span data-ttu-id="35460-543">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="35460-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35460-544">Az.HDInsight</span></span>
* <span data-ttu-id="35460-545">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="35460-546">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="35460-547">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="35460-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="35460-548">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="35460-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="35460-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="35460-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="35460-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="35460-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="35460-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="35460-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="35460-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="35460-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="35460-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="35460-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="35460-554">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="35460-555">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="35460-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="35460-556">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="35460-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="35460-557">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="35460-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="35460-558">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="35460-559">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="35460-560">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="35460-561">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="35460-562">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="35460-563">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="35460-564">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="35460-565">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="35460-566">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="35460-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-567">Az.IotHub</span></span>
* <span data-ttu-id="35460-568">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="35460-568">Breaking changes:</span></span>
    - <span data-ttu-id="35460-569">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="35460-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="35460-570">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="35460-571">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="35460-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="35460-572">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="35460-573">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="35460-574">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="35460-575">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="35460-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="35460-576">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="35460-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="35460-577">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="35460-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="35460-578">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="35460-579">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="35460-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="35460-580">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-582">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="35460-583">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="35460-584">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="35460-585">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="35460-586">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="35460-587">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="35460-588">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="35460-589">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="35460-590">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-591">Az.Resources</span></span>
* <span data-ttu-id="35460-592">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-593">Az.Network</span></span>
* <span data-ttu-id="35460-594">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="35460-595">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="35460-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="35460-601">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="35460-602">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="35460-602">New cmdlet:</span></span>
        - <span data-ttu-id="35460-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="35460-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="35460-604">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="35460-605">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="35460-606">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="35460-607">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="35460-608">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="35460-609">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="35460-610">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="35460-611">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-611">New cmdlets added:</span></span>
        - <span data-ttu-id="35460-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="35460-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="35460-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="35460-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="35460-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="35460-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="35460-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="35460-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="35460-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="35460-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="35460-617">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="35460-618">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="35460-619">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="35460-620">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="35460-621">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="35460-622">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="35460-623">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="35460-624">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-624">New cmdlets added:</span></span>
        - <span data-ttu-id="35460-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="35460-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="35460-626">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="35460-627">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="35460-628">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="35460-629">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="35460-630">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="35460-631">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="35460-632">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="35460-633">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-633">New cmdlets added:</span></span>
        - <span data-ttu-id="35460-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="35460-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="35460-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="35460-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="35460-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="35460-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="35460-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="35460-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="35460-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="35460-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="35460-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="35460-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="35460-640">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="35460-641">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="35460-642">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="35460-643">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="35460-644">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="35460-645">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="35460-646">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="35460-647">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="35460-648">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="35460-649">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="35460-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="35460-650">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="35460-651">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-651">New cmdlets added:</span></span>
        - <span data-ttu-id="35460-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="35460-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="35460-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="35460-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="35460-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="35460-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="35460-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="35460-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35460-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-657">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-658">Az.Sql</span></span>
* <span data-ttu-id="35460-659">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="35460-660">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="35460-661">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="35460-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="35460-662">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="35460-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="35460-663">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="35460-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="35460-664">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="35460-665">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="35460-666">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="35460-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="35460-667">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-668">Az.Storage</span></span>
* <span data-ttu-id="35460-669">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="35460-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="35460-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="35460-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="35460-672">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="35460-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="35460-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="35460-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="35460-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="35460-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="35460-675">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="35460-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="35460-676">Genel</span><span class="sxs-lookup"><span data-stu-id="35460-676">General</span></span>
* <span data-ttu-id="35460-677">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="35460-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-678">Az.Accounts</span></span>
* <span data-ttu-id="35460-679">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="35460-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-680">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-681">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="35460-682">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-683">Az.Automation</span></span>
* <span data-ttu-id="35460-684">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="35460-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35460-685">Az.Batch</span></span>
* <span data-ttu-id="35460-686">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="35460-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-687">Az.Compute</span></span>
* <span data-ttu-id="35460-688">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="35460-689">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="35460-690">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="35460-691">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-692">Az.DataFactory</span></span>
* <span data-ttu-id="35460-693">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="35460-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="35460-694">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="35460-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="35460-695">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-697">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="35460-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="35460-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="35460-699">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="35460-700">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="35460-701">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="35460-702">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-703">Az.IotHub</span></span>
* <span data-ttu-id="35460-704">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="35460-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="35460-705">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="35460-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-706">Az.Monitor</span></span>
* <span data-ttu-id="35460-707">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="35460-708">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="35460-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="35460-709">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="35460-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="35460-710">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-711">Az.Network</span></span>
* <span data-ttu-id="35460-712">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="35460-713">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="35460-714">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-714">New cmdlets added:</span></span>
        - <span data-ttu-id="35460-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="35460-716">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="35460-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="35460-717">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="35460-718">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="35460-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35460-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="35460-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35460-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="35460-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35460-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="35460-722">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="35460-723">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="35460-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="35460-724">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="35460-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="35460-725">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="35460-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="35460-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="35460-726">Az.RedisCache</span></span>
* <span data-ttu-id="35460-727">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-728">Az.Sql</span></span>
* <span data-ttu-id="35460-729">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-730">Az.Storage</span></span>
* <span data-ttu-id="35460-731">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="35460-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="35460-732">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="35460-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="35460-733">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="35460-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="35460-734">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="35460-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="35460-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="35460-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="35460-736">Az.StorageSync</span></span>
* <span data-ttu-id="35460-737">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-738">Az.Websites</span></span>
* <span data-ttu-id="35460-739">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="35460-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="35460-740">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="35460-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="35460-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-741">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-742">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="35460-743">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="35460-744">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="35460-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-745">Az.Automation</span></span>
* <span data-ttu-id="35460-746">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="35460-747">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="35460-748">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-749">Az.Compute</span></span>
* <span data-ttu-id="35460-750">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="35460-751">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="35460-752">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="35460-753">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="35460-754">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="35460-755">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="35460-756">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="35460-757">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="35460-758">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-759">Az.DataFactory</span></span>
* <span data-ttu-id="35460-760">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="35460-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="35460-761">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="35460-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35460-762">Az.HDInsight</span></span>
* <span data-ttu-id="35460-763">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="35460-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-764">Az.IotHub</span></span>
* <span data-ttu-id="35460-765">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="35460-766">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="35460-767">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="35460-767">New cmdlets are:</span></span>
    - <span data-ttu-id="35460-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="35460-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="35460-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="35460-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="35460-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="35460-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="35460-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="35460-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-772">Az.Monitor</span></span>
* <span data-ttu-id="35460-773">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="35460-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="35460-774">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="35460-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="35460-775">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="35460-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="35460-776">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="35460-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="35460-777">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="35460-778">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="35460-779">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="35460-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="35460-780">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="35460-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="35460-781">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="35460-782">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="35460-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="35460-783">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="35460-784">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="35460-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="35460-785">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="35460-786">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="35460-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="35460-787">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="35460-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="35460-788">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="35460-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="35460-789">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="35460-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="35460-790">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="35460-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="35460-791">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="35460-792">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-792">Overall improved help files</span></span>
* <span data-ttu-id="35460-793">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-794">Az.Network</span></span>
* <span data-ttu-id="35460-795">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="35460-796">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="35460-797">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="35460-798">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="35460-799">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="35460-800">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="35460-801">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="35460-802">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="35460-803">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="35460-804">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="35460-805">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="35460-806">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="35460-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="35460-807">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-807">New cmdlets</span></span>
        - <span data-ttu-id="35460-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="35460-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="35460-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="35460-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="35460-810">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="35460-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="35460-811">New-VpnSite</span></span>
        - <span data-ttu-id="35460-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="35460-812">Update-VpnSite</span></span>
        - <span data-ttu-id="35460-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="35460-813">New-VpnConnection</span></span>
        - <span data-ttu-id="35460-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="35460-814">Update-VpnConnection</span></span>
* <span data-ttu-id="35460-815">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-817">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="35460-818">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-819">Az.Resources</span></span>
* <span data-ttu-id="35460-820">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35460-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-822">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="35460-823">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="35460-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="35460-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="35460-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="35460-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="35460-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="35460-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="35460-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="35460-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="35460-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="35460-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="35460-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="35460-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="35460-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="35460-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="35460-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="35460-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="35460-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="35460-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="35460-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="35460-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="35460-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="35460-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="35460-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="35460-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="35460-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="35460-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="35460-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="35460-837">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="35460-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="35460-838">Az.SignalR</span></span>
* <span data-ttu-id="35460-839">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-840">Az.Sql</span></span>
* <span data-ttu-id="35460-841">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="35460-842">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="35460-843">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="35460-844">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="35460-845">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-846">Az.Storage</span></span>
* <span data-ttu-id="35460-847">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="35460-848">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="35460-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="35460-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="35460-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="35460-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="35460-851">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="35460-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="35460-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="35460-853">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="35460-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="35460-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="35460-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="35460-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="35460-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="35460-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="35460-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="35460-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-858">Az.Websites</span></span>
* <span data-ttu-id="35460-859">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="35460-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="35460-860">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="35460-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="35460-861">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="35460-862">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="35460-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="35460-863">Genel</span><span class="sxs-lookup"><span data-stu-id="35460-863">General</span></span>
* <span data-ttu-id="35460-864">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-865">Az.Accounts</span></span>
* <span data-ttu-id="35460-866">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="35460-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="35460-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="35460-867">Az.Aks</span></span>
* <span data-ttu-id="35460-868">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="35460-869">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="35460-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="35460-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-870">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-871">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="35460-872">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="35460-873">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="35460-874">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="35460-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="35460-875">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="35460-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35460-876">Az.Batch</span></span>
* <span data-ttu-id="35460-877">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35460-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35460-878">Az.Cdn</span></span>
* <span data-ttu-id="35460-879">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-880">Az.Compute</span></span>
* <span data-ttu-id="35460-881">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="35460-882">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="35460-883">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="35460-884">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="35460-885">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="35460-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="35460-886">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="35460-887">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="35460-888">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-889">Az.DataFactory</span></span>
* <span data-ttu-id="35460-890">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="35460-891">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="35460-892">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="35460-893">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-895">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35460-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35460-896">Az.EventHub</span></span>
* <span data-ttu-id="35460-897">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="35460-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="35460-898">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="35460-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="35460-899">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="35460-900">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="35460-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="35460-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="35460-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="35460-902">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-903">Az.Monitor</span></span>
* <span data-ttu-id="35460-904">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-905">Az.Network</span></span>
* <span data-ttu-id="35460-906">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="35460-907">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="35460-908">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="35460-909">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="35460-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="35460-910">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="35460-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="35460-911">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="35460-912">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35460-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35460-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="35460-914">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="35460-915">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-915">Added example</span></span>
    - <span data-ttu-id="35460-916">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="35460-917">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="35460-918">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-920">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-921">Az.Resources</span></span>
* <span data-ttu-id="35460-922">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="35460-923">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="35460-924">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="35460-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="35460-925">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35460-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35460-926">Az.ServiceBus</span></span>
* <span data-ttu-id="35460-927">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="35460-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="35460-928">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="35460-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="35460-929">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35460-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-931">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="35460-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="35460-932">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="35460-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="35460-933">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="35460-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="35460-934">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="35460-935">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="35460-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="35460-936">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-937">Az.Sql</span></span>
* <span data-ttu-id="35460-938">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-939">Az.Storage</span></span>
* <span data-ttu-id="35460-940">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="35460-941">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="35460-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="35460-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="35460-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="35460-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="35460-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="35460-944">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="35460-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="35460-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="35460-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-946">Az.Websites</span></span>
* <span data-ttu-id="35460-947">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="35460-948">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="35460-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-949">Az.Accounts</span></span>
* <span data-ttu-id="35460-950">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="35460-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="35460-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="35460-952">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-953">Az.Automation</span></span>
* <span data-ttu-id="35460-954">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35460-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35460-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="35460-956">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-957">Az.Compute</span></span>
* <span data-ttu-id="35460-958">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="35460-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35460-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="35460-960">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="35460-961">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="35460-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-962">Az.DataFactory</span></span>
* <span data-ttu-id="35460-963">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="35460-964">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35460-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35460-965">Az.EventHub</span></span>
* <span data-ttu-id="35460-966">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="35460-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="35460-967">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-968">Az.KeyVault</span></span>
* <span data-ttu-id="35460-969">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35460-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35460-970">Az.LogicApp</span></span>
* <span data-ttu-id="35460-971">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="35460-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="35460-972">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="35460-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="35460-973">Az.ManagedServices</span></span>
* <span data-ttu-id="35460-974">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="35460-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-975">Az.Network</span></span>
* <span data-ttu-id="35460-976">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="35460-977">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-977">New cmdlets</span></span>
        - <span data-ttu-id="35460-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35460-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35460-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35460-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="35460-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35460-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="35460-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="35460-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35460-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="35460-986">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="35460-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="35460-987">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="35460-988">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="35460-989">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="35460-990">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="35460-991">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="35460-992">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-992">Updated cmdlets</span></span>
        - <span data-ttu-id="35460-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35460-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="35460-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35460-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="35460-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35460-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="35460-996">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="35460-997">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="35460-998">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="35460-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35460-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="35460-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35460-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="35460-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35460-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="35460-1002">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="35460-1003">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="35460-1004">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="35460-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35460-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="35460-1006">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="35460-1007">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1009">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="35460-1010">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="35460-1011">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="35460-1012">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="35460-1013">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="35460-1014">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="35460-1015">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="35460-1016">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="35460-1017">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="35460-1018">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1019">Az.Resources</span></span>
- <span data-ttu-id="35460-1020">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="35460-1021">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35460-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35460-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="35460-1023">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="35460-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="35460-1024">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1025">Az.Sql</span></span>
* <span data-ttu-id="35460-1026">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="35460-1027">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="35460-1028">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1029">Az.Storage</span></span>
* <span data-ttu-id="35460-1030">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="35460-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="35460-1031">Az.StorageSync</span></span>
* <span data-ttu-id="35460-1032">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="35460-1033">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1034">Az.Websites</span></span>
* <span data-ttu-id="35460-1035">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="35460-1036">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="35460-1037">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="35460-1038">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1039">Az.Accounts</span></span>
* <span data-ttu-id="35460-1040">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="35460-1041">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="35460-1042">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="35460-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="35460-1043">Az.Advisor</span></span>
* <span data-ttu-id="35460-1044">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="35460-1045">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="35460-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="35460-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-1047">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="35460-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="35460-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="35460-1049">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="35460-1050">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="35460-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="35460-1051">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="35460-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="35460-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="35460-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="35460-1053">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1054">Az.Automation</span></span>
* <span data-ttu-id="35460-1055">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1056">Az.Compute</span></span>
* <span data-ttu-id="35460-1057">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-1058">Az.DataFactory</span></span>
* <span data-ttu-id="35460-1059">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35460-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35460-1060">Az.EventGrid</span></span>
* <span data-ttu-id="35460-1061">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-1062">Az.IotHub</span></span>
* <span data-ttu-id="35460-1063">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1064">Az.Network</span></span>
* <span data-ttu-id="35460-1065">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="35460-1066">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35460-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="35460-1068">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="35460-1069">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="35460-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35460-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="35460-1071">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1073">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="35460-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1074">Az.Resources</span></span>
    - <span data-ttu-id="35460-1075">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="35460-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="35460-1076">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="35460-1077">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="35460-1078">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35460-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35460-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="35460-1080">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1081">Az.Sql</span></span>
* <span data-ttu-id="35460-1082">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="35460-1083">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="35460-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="35460-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="35460-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="35460-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="35460-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="35460-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="35460-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="35460-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="35460-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="35460-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="35460-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="35460-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="35460-1090">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1091">Az.Storage</span></span>
* <span data-ttu-id="35460-1092">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="35460-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="35460-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="35460-1094">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="35460-1095">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="35460-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="35460-1096">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="35460-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="35460-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="35460-1099">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="35460-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="35460-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="35460-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="35460-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="35460-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="35460-1102">Az.StorageSync</span></span>
* <span data-ttu-id="35460-1103">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="35460-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="35460-1104">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1105">Az.Accounts</span></span>
* <span data-ttu-id="35460-1106">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="35460-1107">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="35460-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="35460-1108">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="35460-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="35460-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="35460-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="35460-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1111">Az.Compute</span></span>
* <span data-ttu-id="35460-1112">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="35460-1113">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="35460-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="35460-1114">Az.Dns</span></span>
* <span data-ttu-id="35460-1115">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35460-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35460-1116">Az.EventGrid</span></span>
* <span data-ttu-id="35460-1117">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="35460-1118">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="35460-1118">New cmdlets:</span></span>
    - <span data-ttu-id="35460-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="35460-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="35460-1120">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35460-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="35460-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="35460-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="35460-1122">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="35460-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="35460-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="35460-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="35460-1124">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="35460-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="35460-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="35460-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="35460-1126">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="35460-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="35460-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="35460-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="35460-1128">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="35460-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="35460-1129">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="35460-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="35460-1130">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35460-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="35460-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="35460-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="35460-1132">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="35460-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="35460-1133">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="35460-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="35460-1134">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="35460-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="35460-1135">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="35460-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="35460-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="35460-1137">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="35460-1138">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="35460-1139">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="35460-1140">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="35460-1141">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="35460-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="35460-1142">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="35460-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="35460-1143">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="35460-1144">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="35460-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="35460-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="35460-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="35460-1146">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="35460-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="35460-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="35460-1148">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="35460-1149">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35460-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35460-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="35460-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="35460-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="35460-1152">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="35460-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="35460-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="35460-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="35460-1154">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="35460-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1155">Az.Network</span></span>
* <span data-ttu-id="35460-1156">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="35460-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="35460-1157">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1157">New cmdlets</span></span>
        - <span data-ttu-id="35460-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="35460-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="35460-1159">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="35460-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="35460-1160">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1160">New cmdlets</span></span>
        - <span data-ttu-id="35460-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="35460-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="35460-1162">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="35460-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="35460-1163">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1163">New cmdlets</span></span>
        - <span data-ttu-id="35460-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35460-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="35460-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35460-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="35460-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35460-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="35460-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="35460-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="35460-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35460-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="35460-1169">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="35460-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="35460-1170">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1170">New cmdlets</span></span>
        - <span data-ttu-id="35460-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35460-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35460-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35460-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35460-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35460-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35460-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="35460-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="35460-1175">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="35460-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="35460-1176">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="35460-1177">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="35460-1178">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="35460-1179">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="35460-1180">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="35460-1181">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="35460-1182">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="35460-1183">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="35460-1184">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="35460-1185">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="35460-1186">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="35460-1187">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="35460-1188">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="35460-1189">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="35460-1190">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="35460-1191">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="35460-1192">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="35460-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="35460-1193">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="35460-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="35460-1194">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="35460-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="35460-1195">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="35460-1196">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="35460-1197">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35460-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="35460-1199">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1200">Az.Resources</span></span>
* <span data-ttu-id="35460-1201">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="35460-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="35460-1202">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="35460-1203">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="35460-1204">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35460-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-1206">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1207">Az.Sql</span></span>
* <span data-ttu-id="35460-1208">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="35460-1209">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="35460-1210">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="35460-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="35460-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="35460-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="35460-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="35460-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="35460-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="35460-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="35460-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="35460-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="35460-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1216">Az.Storage</span></span>
* <span data-ttu-id="35460-1217">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="35460-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="35460-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="35460-1219">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="35460-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1221">Az.Websites</span></span>
* <span data-ttu-id="35460-1222">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="35460-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="35460-1223">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="35460-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="35460-1224">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="35460-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35460-1225">Az.Cdn</span></span>
* <span data-ttu-id="35460-1226">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1227">Az.Compute</span></span>
* <span data-ttu-id="35460-1228">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="35460-1229">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="35460-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35460-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35460-1230">Az.EventHub</span></span>
* <span data-ttu-id="35460-1231">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="35460-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="35460-1232">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="35460-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1233">Az.Network</span></span>
* <span data-ttu-id="35460-1234">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="35460-1235">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35460-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="35460-1237">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1239">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35460-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35460-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="35460-1241">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="35460-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35460-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-1243">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="35460-1244">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1245">Az.Sql</span></span>
* <span data-ttu-id="35460-1246">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="35460-1247">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="35460-1248">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="35460-1249">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="35460-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1250">Az.Websites</span></span>
* <span data-ttu-id="35460-1251">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="35460-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="35460-1252">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="35460-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-1254">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="35460-1255">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="35460-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="35460-1256">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="35460-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="35460-1257">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="35460-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="35460-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="35460-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="35460-1259">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="35460-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="35460-1260">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="35460-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="35460-1261">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="35460-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="35460-1262">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="35460-1263">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="35460-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="35460-1264">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="35460-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="35460-1265">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="35460-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="35460-1266">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="35460-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="35460-1267">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="35460-1268">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="35460-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="35460-1269">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="35460-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="35460-1270">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="35460-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="35460-1271">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="35460-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="35460-1272">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="35460-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="35460-1273">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="35460-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="35460-1274">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="35460-1275">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="35460-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="35460-1276">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="35460-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="35460-1277">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="35460-1278">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="35460-1279">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="35460-1280">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="35460-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="35460-1281">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="35460-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="35460-1282">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="35460-1283">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="35460-1284">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="35460-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="35460-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="35460-1286">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="35460-1287">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="35460-1288">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="35460-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="35460-1289">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="35460-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="35460-1290">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="35460-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="35460-1291">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="35460-1292">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="35460-1293">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="35460-1294">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="35460-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="35460-1295">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="35460-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="35460-1296">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="35460-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="35460-1297">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="35460-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="35460-1298">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="35460-1299">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="35460-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="35460-1300">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="35460-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="35460-1301">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="35460-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="35460-1302">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="35460-1303">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="35460-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="35460-1304">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="35460-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="35460-1305">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="35460-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="35460-1306">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="35460-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="35460-1307">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="35460-1308">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="35460-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="35460-1309">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="35460-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="35460-1310">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="35460-1311">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="35460-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="35460-1312">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="35460-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="35460-1313">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="35460-1314">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="35460-1315">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="35460-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="35460-1316">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="35460-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="35460-1317">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="35460-1318">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="35460-1319">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="35460-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="35460-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="35460-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="35460-1321">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="35460-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="35460-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="35460-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="35460-1323">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="35460-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="35460-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="35460-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="35460-1325">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="35460-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="35460-1326">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="35460-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="35460-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="35460-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="35460-1328">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="35460-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="35460-1329">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="35460-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="35460-1330">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="35460-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1331">Az.Automation</span></span>
* <span data-ttu-id="35460-1332">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="35460-1333">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="35460-1334">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="35460-1335">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="35460-1336">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="35460-1337">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="35460-1338">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1339">Az.Compute</span></span>
* <span data-ttu-id="35460-1340">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="35460-1341">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="35460-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-1343">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-1344">Az.Monitor</span></span>
* <span data-ttu-id="35460-1345">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1346">Az.Network</span></span>
* <span data-ttu-id="35460-1347">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="35460-1348">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="35460-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="35460-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="35460-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="35460-1350">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1351">Az.Resources</span></span>
* <span data-ttu-id="35460-1352">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1353">Az.Sql</span></span>
* <span data-ttu-id="35460-1354">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="35460-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="35460-1355">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1356">Az.Accounts</span></span>
* <span data-ttu-id="35460-1357">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="35460-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35460-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35460-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="35460-1359">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="35460-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="35460-1360">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="35460-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1361">Az.Compute</span></span>
* <span data-ttu-id="35460-1362">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="35460-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="35460-1363">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="35460-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="35460-1364">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="35460-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="35460-1365">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="35460-1366">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="35460-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="35460-1367">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="35460-1368">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="35460-1368">Breaking changes</span></span>
    - <span data-ttu-id="35460-1369">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="35460-1370">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="35460-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="35460-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="35460-1372">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="35460-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="35460-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="35460-1373">Az.Dns</span></span>
* <span data-ttu-id="35460-1374">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="35460-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="35460-1375">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="35460-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="35460-1376">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35460-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35460-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="35460-1378">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="35460-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="35460-1379">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="35460-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="35460-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35460-1380">Az.HDInsight</span></span>
* <span data-ttu-id="35460-1381">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="35460-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="35460-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="35460-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="35460-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="35460-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="35460-1384">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="35460-1385">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="35460-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="35460-1386">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="35460-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="35460-1387">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="35460-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-1388">Az.Monitor</span></span>
* <span data-ttu-id="35460-1389">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="35460-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="35460-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="35460-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="35460-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="35460-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="35460-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="35460-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="35460-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="35460-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="35460-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="35460-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="35460-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="35460-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="35460-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35460-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35460-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35460-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35460-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35460-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35460-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35460-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35460-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35460-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35460-1401">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="35460-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="35460-1402">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1403">Az.Network</span></span>
* <span data-ttu-id="35460-1404">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="35460-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="35460-1405">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1405">New cmdlets</span></span>
        - <span data-ttu-id="35460-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35460-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="35460-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35460-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="35460-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35460-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="35460-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35460-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="35460-1410">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="35460-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="35460-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="35460-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="35460-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="35460-1413">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="35460-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="35460-1414">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="35460-1415">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35460-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="35460-1417">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="35460-1418">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="35460-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="35460-1419">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="35460-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1421">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="35460-1422">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="35460-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="35460-1423">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="35460-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="35460-1424">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="35460-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="35460-1425">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="35460-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="35460-1426">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="35460-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="35460-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="35460-1427">Az.Relay</span></span>
* <span data-ttu-id="35460-1428">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="35460-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35460-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35460-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="35460-1430">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1431">Az.Storage</span></span>
* <span data-ttu-id="35460-1432">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="35460-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="35460-1433">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="35460-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="35460-1434">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="35460-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="35460-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="35460-1436">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="35460-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="35460-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="35460-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="35460-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1440">Az.Websites</span></span>
* <span data-ttu-id="35460-1441">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="35460-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="35460-1442">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="35460-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="35460-1443">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35460-1444">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="35460-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="35460-1445">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="35460-1446">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="35460-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="35460-1447">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="35460-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="35460-1448">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="35460-1449">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35460-1450">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="35460-1451">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1452">Az.Accounts</span></span>
* <span data-ttu-id="35460-1453">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="35460-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35460-1454">Az.Batch</span></span>
* <span data-ttu-id="35460-1455">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35460-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35460-1456">Az.Cdn</span></span>
* <span data-ttu-id="35460-1457">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35460-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35460-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="35460-1459">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1460">Az.Compute</span></span>
* <span data-ttu-id="35460-1461">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="35460-1462">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35460-1463">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-1464">Az.DataFactory</span></span>
* <span data-ttu-id="35460-1465">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-1467">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35460-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35460-1468">Az.EventGrid</span></span>
* <span data-ttu-id="35460-1469">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35460-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35460-1470">Az.EventHub</span></span>
* <span data-ttu-id="35460-1471">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="35460-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35460-1472">Az.HDInsight</span></span>
* <span data-ttu-id="35460-1473">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-1474">Az.IotHub</span></span>
* <span data-ttu-id="35460-1475">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-1476">Az.KeyVault</span></span>
* <span data-ttu-id="35460-1477">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35460-1478">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="35460-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="35460-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="35460-1480">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="35460-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="35460-1481">Az.Media</span></span>
* <span data-ttu-id="35460-1482">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-1483">Az.Monitor</span></span>
  * <span data-ttu-id="35460-1484">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="35460-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="35460-1485">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="35460-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="35460-1486">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="35460-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="35460-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="35460-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="35460-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="35460-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="35460-1489">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="35460-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="35460-1490">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1491">Az.Network</span></span>
* <span data-ttu-id="35460-1492">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35460-1493">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="35460-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="35460-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="35460-1495">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35460-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="35460-1497">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="35460-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="35460-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="35460-1499">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1501">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35460-1502">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="35460-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="35460-1503">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="35460-1504">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="35460-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="35460-1505">Az.RedisCache</span></span>
* <span data-ttu-id="35460-1506">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1507">Az.Resources</span></span>
* <span data-ttu-id="35460-1508">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1509">Az.Sql</span></span>
* <span data-ttu-id="35460-1510">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="35460-1511">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35460-1512">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="35460-1513">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="35460-1514">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="35460-1515">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="35460-1516">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1517">Az.Websites</span></span>
* <span data-ttu-id="35460-1518">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="35460-1519">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35460-1520">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="35460-1521">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="35460-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="35460-1522">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35460-1523">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="35460-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="35460-1524">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="35460-1525">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="35460-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="35460-1526">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="35460-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="35460-1527">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="35460-1528">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35460-1529">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="35460-1530">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35460-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1531">Az.Accounts</span></span>
* <span data-ttu-id="35460-1532">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="35460-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35460-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="35460-1534">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="35460-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="35460-1535">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="35460-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1536">Az.Automation</span></span>
* <span data-ttu-id="35460-1537">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="35460-1538">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="35460-1539">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="35460-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1540">Az.Compute</span></span>
* <span data-ttu-id="35460-1541">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="35460-1542">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="35460-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="35460-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="35460-1544">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-1545">Az.DataFactory</span></span>
* <span data-ttu-id="35460-1546">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="35460-1547">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1548">Az.Resources</span></span>
* <span data-ttu-id="35460-1549">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="35460-1550">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="35460-1551">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="35460-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="35460-1552">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="35460-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="35460-1553">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="35460-1554">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="35460-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1555">Az.Sql</span></span>
* <span data-ttu-id="35460-1556">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1557">Az.Storage</span></span>
* <span data-ttu-id="35460-1558">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="35460-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="35460-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="35460-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="35460-1560">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="35460-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="35460-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="35460-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="35460-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="35460-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="35460-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="35460-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="35460-1565">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="35460-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="35460-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="35460-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="35460-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="35460-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="35460-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="35460-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="35460-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="35460-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="35460-1570">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35460-1571">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="35460-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="35460-1572">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="35460-1573">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="35460-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="35460-1574">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="35460-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="35460-1575">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="35460-1576">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35460-1577">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="35460-1578">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1579">Az.Automation</span></span>
* <span data-ttu-id="35460-1580">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="35460-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="35460-1581">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="35460-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="35460-1582">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="35460-1582">Pre-Post script</span></span>
    * <span data-ttu-id="35460-1583">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="35460-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1584">Az.Compute</span></span>
* <span data-ttu-id="35460-1585">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="35460-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="35460-1586">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-1587">Az.KeyVault</span></span>
* <span data-ttu-id="35460-1588">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1589">Az.Network</span></span>
* <span data-ttu-id="35460-1590">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="35460-1591">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1593">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="35460-1594">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1595">Az.Resources</span></span>
* <span data-ttu-id="35460-1596">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="35460-1597">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1598">Az.Sql</span></span>
* <span data-ttu-id="35460-1599">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1600">Az.Storage</span></span>
* <span data-ttu-id="35460-1601">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="35460-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="35460-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="35460-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="35460-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="35460-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="35460-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="35460-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="35460-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="35460-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="35460-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1608">Az.Websites</span></span>
* <span data-ttu-id="35460-1609">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="35460-1610">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1611">Az.Accounts</span></span>
* <span data-ttu-id="35460-1612">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="35460-1613">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1614">Az.Automation</span></span>
* <span data-ttu-id="35460-1615">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="35460-1616">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="35460-1617">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="35460-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35460-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35460-1618">Az.Cdn</span></span>
* <span data-ttu-id="35460-1619">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1620">Az.Compute</span></span>
* <span data-ttu-id="35460-1621">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-1622">Az.DataFactory</span></span>
* <span data-ttu-id="35460-1623">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35460-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35460-1624">Az.LogicApp</span></span>
* <span data-ttu-id="35460-1625">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="35460-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1626">Az.Network</span></span>
* <span data-ttu-id="35460-1627">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1629">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="35460-1630">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="35460-1630">SDK Update</span></span>
* <span data-ttu-id="35460-1631">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="35460-1632">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1633">Az.Resources</span></span>
* <span data-ttu-id="35460-1634">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="35460-1635">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="35460-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="35460-1636">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="35460-1637">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="35460-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="35460-1638">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="35460-1639">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="35460-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1640">Az.Sql</span></span>
* <span data-ttu-id="35460-1641">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="35460-1642">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1643">Az.Storage</span></span>
* <span data-ttu-id="35460-1644">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35460-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="35460-1645">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="35460-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35460-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="35460-1647">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1648">Az.Automation</span></span>
* <span data-ttu-id="35460-1649">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="35460-1650">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="35460-1651">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35460-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35460-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="35460-1653">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1654">Az.Compute</span></span>
* <span data-ttu-id="35460-1655">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="35460-1656">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="35460-1657">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="35460-1658">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="35460-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-1660">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35460-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35460-1661">Az.EventHub</span></span>
* <span data-ttu-id="35460-1662">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-1663">Az.KeyVault</span></span>
* <span data-ttu-id="35460-1664">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35460-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35460-1665">Az.LogicApp</span></span>
* <span data-ttu-id="35460-1666">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="35460-1667">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="35460-1668">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="35460-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35460-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="35460-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35460-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="35460-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35460-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="35460-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35460-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="35460-1673">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="35460-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="35460-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35460-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="35460-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35460-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="35460-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35460-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="35460-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35460-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="35460-1678">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35460-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-1679">Az.Monitor</span></span>
* <span data-ttu-id="35460-1680">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1681">Az.Network</span></span>
* <span data-ttu-id="35460-1682">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35460-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="35460-1684">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="35460-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="35460-1685">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="35460-1686">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1687">Az.Resources</span></span>
* <span data-ttu-id="35460-1688">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="35460-1689">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="35460-1690">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="35460-1691">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1692">Az.Sql</span></span>
* <span data-ttu-id="35460-1693">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="35460-1694">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1695">Az.Websites</span></span>
* <span data-ttu-id="35460-1696">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="35460-1697">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1698">Az.Accounts</span></span>
* <span data-ttu-id="35460-1699">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="35460-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="35460-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35460-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="35460-1701">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="35460-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1702">Az.Compute</span></span>
* <span data-ttu-id="35460-1703">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="35460-1704">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="35460-1705">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="35460-1707">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="35460-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1708">Az.Resources</span></span>
* <span data-ttu-id="35460-1709">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="35460-1710">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="35460-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="35460-1711">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="35460-1712">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="35460-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1713">Az.Sql</span></span>
* <span data-ttu-id="35460-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35460-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="35460-1715">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="35460-1716">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="35460-1717">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1718">Az.Accounts</span></span>
* <span data-ttu-id="35460-1719">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="35460-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="35460-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35460-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="35460-1721">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="35460-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="35460-1723">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="35460-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="35460-1724">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1725">Az.Accounts</span></span>
* <span data-ttu-id="35460-1726">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35460-1727">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35460-1728">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="35460-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="35460-1729">Az.Aks</span></span>
* <span data-ttu-id="35460-1730">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35460-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1731">Az.Automation</span></span>
* <span data-ttu-id="35460-1732">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="35460-1733">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35460-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35460-1734">Az.Cdn</span></span>
* <span data-ttu-id="35460-1735">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1736">Az.Compute</span></span>
* <span data-ttu-id="35460-1737">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="35460-1738">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="35460-1739">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="35460-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35460-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="35460-1741">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35460-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35460-1742">Az.DataFactory</span></span>
* <span data-ttu-id="35460-1743">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-1745">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="35460-1746">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="35460-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="35460-1747">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-1748">Az.IotHub</span></span>
* <span data-ttu-id="35460-1749">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35460-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-1750">Az.KeyVault</span></span>
* <span data-ttu-id="35460-1751">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1752">Az.Network</span></span>
* <span data-ttu-id="35460-1753">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1754">Az.Resources</span></span>
* <span data-ttu-id="35460-1755">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="35460-1756">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="35460-1757">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="35460-1758">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="35460-1759">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="35460-1760">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="35460-1761">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="35460-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35460-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-1763">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="35460-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="35460-1764">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1764">Fix some error messages.</span></span>
* <span data-ttu-id="35460-1765">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="35460-1766">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="35460-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="35460-1767">Az.SignalR</span></span>
* <span data-ttu-id="35460-1768">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1769">Az.Sql</span></span>
* <span data-ttu-id="35460-1770">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35460-1771">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="35460-1772">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="35460-1773">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="35460-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1774">Az.Storage</span></span>
* <span data-ttu-id="35460-1775">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35460-1776">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="35460-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="35460-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="35460-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="35460-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="35460-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="35460-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="35460-1780">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1781">Az.Websites</span></span>
* <span data-ttu-id="35460-1782">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35460-1783">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="35460-1784">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="35460-1785">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="35460-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35460-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1786">Az.Accounts</span></span>
* <span data-ttu-id="35460-1787">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1788">Az.Compute</span></span>
* <span data-ttu-id="35460-1789">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="35460-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="35460-1790">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="35460-1791">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="35460-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-1793">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="35460-1794">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35460-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35460-1795">Az.EventGrid</span></span>
* <span data-ttu-id="35460-1796">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="35460-1797">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="35460-1798">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="35460-1799">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="35460-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="35460-1800">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="35460-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="35460-1801">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="35460-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="35460-1802">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="35460-1803">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="35460-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="35460-1804">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="35460-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="35460-1805">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="35460-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="35460-1806">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="35460-1807">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35460-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35460-1808">Az.IotHub</span></span>
* <span data-ttu-id="35460-1809">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35460-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35460-1810">Az.LogicApp</span></span>
* <span data-ttu-id="35460-1811">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="35460-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1812">Az.Resources</span></span>
* <span data-ttu-id="35460-1813">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="35460-1814">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="35460-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="35460-1815">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="35460-1816">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="35460-1817">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="35460-1818">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="35460-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="35460-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="35460-1819">Az.SignalR</span></span>
* <span data-ttu-id="35460-1820">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="35460-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1821">Az.Sql</span></span>
* <span data-ttu-id="35460-1822">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="35460-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35460-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1823">Az.Storage</span></span>
* <span data-ttu-id="35460-1824">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="35460-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="35460-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="35460-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="35460-1826">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="35460-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="35460-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1828">Az.Websites</span></span>
* <span data-ttu-id="35460-1829">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="35460-1830">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="35460-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="35460-1831">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="35460-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="35460-1832">Genel</span><span class="sxs-lookup"><span data-stu-id="35460-1832">General</span></span>

- <span data-ttu-id="35460-1833">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="35460-1834">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="35460-1834">Online help for each module</span></span>
- <span data-ttu-id="35460-1835">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="35460-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="35460-1836">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="35460-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35460-1837">Az.Accounts</span></span>
- <span data-ttu-id="35460-1838">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35460-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="35460-1839">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="35460-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="35460-1841">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="35460-1841">Fixes for #7002</span></span>
- <span data-ttu-id="35460-1842">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="35460-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35460-1843">Az.Batch</span></span>
- <span data-ttu-id="35460-1844">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="35460-1845">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="35460-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="35460-1846">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="35460-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="35460-1847">Az.Billing</span></span>
- <span data-ttu-id="35460-1848">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="35460-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="35460-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="35460-1850">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="35460-1851">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="35460-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="35460-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="35460-1853">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="35460-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="35460-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="35460-1855">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="35460-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="35460-1857">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="35460-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35460-1858">Az.Monitor</span></span>
- <span data-ttu-id="35460-1859">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="35460-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35460-1860">Az.KeyVault</span></span>
- <span data-ttu-id="35460-1861">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="35460-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="35460-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="35460-1863">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="35460-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="35460-1864">Az.Media</span></span>
- <span data-ttu-id="35460-1865">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="35460-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="35460-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1866">Az.Network</span></span>
<span data-ttu-id="35460-1867">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="35460-1868">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="35460-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="35460-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35460-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35460-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35460-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35460-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35460-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35460-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35460-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35460-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35460-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35460-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="35460-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="35460-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="35460-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="35460-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="35460-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="35460-1877">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="35460-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35460-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="35460-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35460-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="35460-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35460-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="35460-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35460-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="35460-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="35460-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="35460-1883">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="35460-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="35460-1884">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="35460-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="35460-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="35460-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="35460-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="35460-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="35460-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="35460-1888">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="35460-1889">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="35460-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35460-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="35460-1891">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="35460-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35460-1892">Az.Profile</span></span>
- <span data-ttu-id="35460-1893">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="35460-1895">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="35460-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1896">Az.Resources</span></span>
- <span data-ttu-id="35460-1897">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="35460-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="35460-1899">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="35460-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="35460-1900">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="35460-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="35460-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="35460-1902">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="35460-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="35460-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1903">Az.Sql</span></span>
- <span data-ttu-id="35460-1904">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="35460-1905">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="35460-1906">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="35460-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1907">Az.Storage</span></span>
- <span data-ttu-id="35460-1908">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="35460-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1909">Az.Websites</span></span>
- <span data-ttu-id="35460-1910">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="35460-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="35460-1911">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="35460-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="35460-1912">Genel</span><span class="sxs-lookup"><span data-stu-id="35460-1912">General</span></span>

* <span data-ttu-id="35460-1913">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="35460-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="35460-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1914">Az.Compute</span></span>

* <span data-ttu-id="35460-1915">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="35460-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="35460-1917">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="35460-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35460-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="35460-1919">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="35460-1920">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="35460-1921">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="35460-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35460-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="35460-1923">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="35460-1924">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="35460-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1925">Az.Resources</span></span>

* <span data-ttu-id="35460-1926">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="35460-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="35460-1927">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="35460-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1928">Az.Sql</span></span>

* <span data-ttu-id="35460-1929">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="35460-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="35460-1930">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="35460-1931">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="35460-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35460-1932">Az.Storage</span></span>

* <span data-ttu-id="35460-1933">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="35460-1934">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="35460-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="35460-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="35460-1936">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="35460-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="35460-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="35460-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="35460-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="35460-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-1939">Az.Websites</span></span>

* <span data-ttu-id="35460-1940">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="35460-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="35460-1941">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="35460-1942">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="35460-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="35460-1943">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="35460-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="35460-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35460-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="35460-1945">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="35460-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="35460-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35460-1946">Az.Automation</span></span>
* <span data-ttu-id="35460-1947">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="35460-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="35460-1948">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="35460-1949">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="35460-1950">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="35460-1951">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="35460-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-1952">Az.Compute</span></span>
* <span data-ttu-id="35460-1953">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="35460-1954">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="35460-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="35460-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="35460-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="35460-1956">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="35460-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="35460-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="35460-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="35460-1958">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="35460-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-1959">Az.Network</span></span>
* <span data-ttu-id="35460-1960">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="35460-1961">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="35460-1962">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="35460-1963">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="35460-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="35460-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="35460-1965">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="35460-1966">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="35460-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="35460-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="35460-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="35460-1968">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="35460-1969">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="35460-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="35460-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="35460-1970">Az.Relay</span></span>
* <span data-ttu-id="35460-1971">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="35460-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-1972">Az.Resources</span></span>
* <span data-ttu-id="35460-1973">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="35460-1974">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="35460-1975">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="35460-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="35460-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-1977">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="35460-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-1978">Az.Sql</span></span>
* <span data-ttu-id="35460-1979">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="35460-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35460-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35460-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35460-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35460-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35460-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35460-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35460-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35460-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35460-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="35460-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35460-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="35460-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35460-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="35460-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35460-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="35460-1988">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="35460-1989">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="35460-1990">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="35460-1991">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="35460-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="35460-1992">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="35460-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="35460-1993">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="35460-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="35460-1994">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="35460-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="35460-1995">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="35460-1996">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="35460-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="35460-1997">Genel</span><span class="sxs-lookup"><span data-stu-id="35460-1997">General</span></span>
* <span data-ttu-id="35460-1998">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="35460-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="35460-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35460-1999">Az.Profile</span></span>
* <span data-ttu-id="35460-2000">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="35460-2001">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="35460-2002">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="35460-2003">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="35460-2004">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="35460-2005">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="35460-2006">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="35460-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35460-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="35460-2008">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-2009">Az.Compute</span></span>
* <span data-ttu-id="35460-2010">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="35460-2011">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="35460-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="35460-2012">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-2014">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="35460-2015">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="35460-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="35460-2016">Az.Insights</span></span>
* <span data-ttu-id="35460-2017">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="35460-2018">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="35460-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="35460-2019">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="35460-2020">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="35460-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-2021">Az.Network</span></span>
* <span data-ttu-id="35460-2022">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="35460-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="35460-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="35460-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="35460-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="35460-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="35460-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="35460-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="35460-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="35460-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="35460-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="35460-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="35460-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="35460-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35460-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35460-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="35460-2030">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-2031">Az.Resources</span></span>
* <span data-ttu-id="35460-2032">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="35460-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="35460-2033">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="35460-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35460-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35460-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="35460-2035">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35460-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35460-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="35460-2037">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="35460-2038">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="35460-2039">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="35460-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="35460-2040">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="35460-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="35460-2041">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="35460-2042">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="35460-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="35460-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35460-2043">Az.Profile</span></span>
* <span data-ttu-id="35460-2044">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="35460-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="35460-2045">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="35460-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-2046">Az.Compute</span></span>
* <span data-ttu-id="35460-2047">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="35460-2048">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35460-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35460-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="35460-2050">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="35460-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="35460-2051">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="35460-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="35460-2052">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="35460-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="35460-2053">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="35460-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="35460-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="35460-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-2055">Az.Network</span></span>
* <span data-ttu-id="35460-2056">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="35460-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="35460-2057">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-2058">Az.Resources</span></span>
* <span data-ttu-id="35460-2059">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="35460-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="35460-2060">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="35460-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="35460-2061">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="35460-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="35460-2062">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="35460-2062">Azure.Storage</span></span>
* <span data-ttu-id="35460-2063">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="35460-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="35460-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="35460-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="35460-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="35460-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="35460-2066">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="35460-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="35460-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="35460-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35460-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35460-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="35460-2069">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="35460-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35460-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35460-2070">Az.Compute</span></span>
* <span data-ttu-id="35460-2071">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="35460-2072">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="35460-2073">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="35460-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="35460-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="35460-2075">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="35460-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35460-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35460-2076">Az.Network</span></span>
* <span data-ttu-id="35460-2077">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="35460-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="35460-2078">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2078">new cmdlets added</span></span>
    - <span data-ttu-id="35460-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35460-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="35460-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35460-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="35460-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35460-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="35460-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35460-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="35460-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="35460-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="35460-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="35460-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="35460-2085">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="35460-2086">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="35460-2087">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="35460-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="35460-2088">Az.RedisCache</span></span>
* <span data-ttu-id="35460-2089">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="35460-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="35460-2090">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="35460-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35460-2091">Az.Resources</span></span>
* <span data-ttu-id="35460-2092">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="35460-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="35460-2093">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="35460-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35460-2094">Az.Sql</span></span>
* <span data-ttu-id="35460-2095">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="35460-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35460-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35460-2096">Az.Websites</span></span>
* <span data-ttu-id="35460-2097">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="35460-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="35460-2098">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="35460-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="35460-2099">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="35460-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="35460-2100">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="35460-2100">Initial Release</span></span>
