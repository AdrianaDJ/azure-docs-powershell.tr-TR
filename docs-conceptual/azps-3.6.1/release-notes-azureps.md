---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 4c7ea19a225d63307ecf4a6fe5ebfa14ccd78d7e
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79036170"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0eedb-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="0eedb-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="0eedb-104">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="0eedb-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-105">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-106">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="0eedb-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="0eedb-107">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="0eedb-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="0eedb-108">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0eedb-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-109">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-110">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="0eedb-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="0eedb-111">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="0eedb-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="0eedb-112">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="0eedb-113">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="0eedb-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-115">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-116">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-117">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0eedb-118">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0eedb-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="0eedb-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0eedb-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0eedb-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0eedb-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="0eedb-123">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="0eedb-124">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0eedb-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="0eedb-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0eedb-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="0eedb-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0eedb-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="0eedb-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0eedb-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="0eedb-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0eedb-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="0eedb-129">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0eedb-130">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0eedb-131">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="0eedb-132">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0eedb-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="0eedb-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0eedb-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="0eedb-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0eedb-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="0eedb-135">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-136">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-137">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="0eedb-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-138">Az.Network</span></span>
* <span data-ttu-id="0eedb-139">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="0eedb-140">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="0eedb-141">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="0eedb-142">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-143">Az.Resources</span></span>
* <span data-ttu-id="0eedb-144">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="0eedb-145">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="0eedb-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="0eedb-146">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="0eedb-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="0eedb-147">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="0eedb-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="0eedb-148">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="0eedb-149">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="0eedb-150">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="0eedb-151">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="0eedb-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eedb-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0eedb-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eedb-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0eedb-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eedb-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="0eedb-155">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="0eedb-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0eedb-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="0eedb-157">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-157">Brought ScopedDeployment from SDK 3.3.0</span></span> 

#### <a name="azsql"></a><span data-ttu-id="0eedb-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-158">Az.Sql</span></span>
* <span data-ttu-id="0eedb-159">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="0eedb-160">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="0eedb-161">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="0eedb-161">Get/Set LTR policy on a managed database</span></span> 
    - <span data-ttu-id="0eedb-162">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="0eedb-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span> 
    - <span data-ttu-id="0eedb-163">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-163">Remove an LTR backup</span></span> 
    - <span data-ttu-id="0eedb-164">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="0eedb-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="0eedb-165">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="0eedb-166">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="0eedb-167">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-168">Az.Storage</span></span>
* <span data-ttu-id="0eedb-169">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="0eedb-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="0eedb-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="0eedb-171">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="0eedb-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0eedb-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="0eedb-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0eedb-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-174">Az.Websites</span></span>
* <span data-ttu-id="0eedb-175">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="0eedb-176">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="0eedb-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="0eedb-177">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="0eedb-178">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="0eedb-179">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="0eedb-180">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="0eedb-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eedb-181">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0eedb-181">Highlights since the last major release</span></span>
* <span data-ttu-id="0eedb-182">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="0eedb-183">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="0eedb-184">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-185">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-186">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-187">Az.Automation</span></span>
* <span data-ttu-id="0eedb-188">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eedb-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eedb-190">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="0eedb-191">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-192">Az.Compute</span></span>
* <span data-ttu-id="0eedb-193">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0eedb-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eedb-194">Az.FrontDoor</span></span>
* <span data-ttu-id="0eedb-195">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-196">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-197">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0eedb-198">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0eedb-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="0eedb-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0eedb-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0eedb-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0eedb-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0eedb-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-203">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-204">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-205">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-206">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="0eedb-207">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="0eedb-208">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-209">Az.Network</span></span>
* <span data-ttu-id="0eedb-210">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="0eedb-211">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0eedb-212">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0eedb-213">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="0eedb-214">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-214">No new cmdlets are added.</span></span> <span data-ttu-id="0eedb-215">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-217">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-218">Az.Resources</span></span>
* <span data-ttu-id="0eedb-219">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="0eedb-220">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0eedb-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="0eedb-221">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0eedb-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="0eedb-222">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="0eedb-223">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="0eedb-224">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="0eedb-225">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="0eedb-226">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-227">Az.Sql</span></span>
* <span data-ttu-id="0eedb-228">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="0eedb-229">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="0eedb-230">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0eedb-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0eedb-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0eedb-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0eedb-232">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0eedb-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0eedb-233">Az.StorageSync</span></span>
* <span data-ttu-id="0eedb-234">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0eedb-235">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="0eedb-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eedb-236">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0eedb-236">Highlights since the last major release</span></span>
* <span data-ttu-id="0eedb-237">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0eedb-238">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-239">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-240">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="0eedb-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0eedb-241">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0eedb-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-242">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-243">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0eedb-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0eedb-244">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="0eedb-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="0eedb-245">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0eedb-246">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-247">Az.Compute</span></span>
* <span data-ttu-id="0eedb-248">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="0eedb-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0eedb-249">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0eedb-250">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0eedb-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0eedb-252">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-253">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-254">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0eedb-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0eedb-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="0eedb-256">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0eedb-257">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0eedb-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0eedb-258">Az.HDInsight</span></span>
* <span data-ttu-id="0eedb-259">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-260">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-261">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-262">Az.Network</span></span>
* <span data-ttu-id="0eedb-263">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0eedb-264">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="0eedb-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0eedb-265">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0eedb-266">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0eedb-267">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="0eedb-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0eedb-268">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0eedb-269">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0eedb-270">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0eedb-271">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-271">New cmdlets added:</span></span>
        - <span data-ttu-id="0eedb-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eedb-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0eedb-273">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0eedb-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0eedb-275">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0eedb-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="0eedb-277">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="0eedb-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0eedb-278">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0eedb-279">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0eedb-280">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-282">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0eedb-283">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-284">Az.Resources</span></span>
* <span data-ttu-id="0eedb-285">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0eedb-286">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-287">Az.Sql</span></span>
<span data-ttu-id="0eedb-288">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-289">Az.Storage</span></span>
* <span data-ttu-id="0eedb-290">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0eedb-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0eedb-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="0eedb-292">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0eedb-293">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-294">Az.Websites</span></span>
* <span data-ttu-id="0eedb-295">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="0eedb-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0eedb-296">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0eedb-297">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="0eedb-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-298">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-299">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eedb-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eedb-300">Az.Cdn</span></span>
* <span data-ttu-id="0eedb-301">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="0eedb-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-302">Az.Compute</span></span>
* <span data-ttu-id="0eedb-303">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0eedb-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="0eedb-305">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0eedb-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0eedb-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0eedb-307">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0eedb-308">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="0eedb-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0eedb-309">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0eedb-310">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0eedb-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0eedb-311">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0eedb-312">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0eedb-313">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0eedb-314">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0eedb-315">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0eedb-316">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="0eedb-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0eedb-317">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0eedb-318">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="0eedb-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0eedb-319">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0eedb-320">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0eedb-321">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0eedb-322">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0eedb-323">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0eedb-324">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="0eedb-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-325">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-326">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0eedb-327">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0eedb-328">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0eedb-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0eedb-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="0eedb-330">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eedb-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-331">Az.EventHub</span></span>
* <span data-ttu-id="0eedb-332">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0eedb-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0eedb-333">Az.HDInsight</span></span>
* <span data-ttu-id="0eedb-334">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0eedb-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0eedb-335">Az.MachineLearning</span></span>
* <span data-ttu-id="0eedb-336">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0eedb-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0eedb-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0eedb-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0eedb-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0eedb-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0eedb-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0eedb-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0eedb-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0eedb-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0eedb-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0eedb-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="0eedb-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0eedb-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="0eedb-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-344">Az.Network</span></span>
* <span data-ttu-id="0eedb-345">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-347">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0eedb-348">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0eedb-349">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0eedb-350">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-351">Az.Resources</span></span>
* <span data-ttu-id="0eedb-352">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-353">Az.Sql</span></span>
* <span data-ttu-id="0eedb-354">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0eedb-355">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0eedb-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0eedb-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0eedb-357">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-358">Az.Storage</span></span>
* <span data-ttu-id="0eedb-359">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0eedb-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0eedb-361">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0eedb-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="0eedb-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0eedb-363">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0eedb-364">Genel</span><span class="sxs-lookup"><span data-stu-id="0eedb-364">General</span></span>
* <span data-ttu-id="0eedb-365">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-366">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-367">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0eedb-368">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0eedb-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eedb-369">Az.Batch</span></span>
* <span data-ttu-id="0eedb-370">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-371">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-372">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0eedb-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eedb-373">Az.FrontDoor</span></span>
* <span data-ttu-id="0eedb-374">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0eedb-375">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0eedb-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0eedb-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="0eedb-377">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="0eedb-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-378">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-379">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0eedb-380">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="0eedb-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0eedb-381">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-382">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-383">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0eedb-384">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="0eedb-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0eedb-385">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="0eedb-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-386">Az.Network</span></span>
* <span data-ttu-id="0eedb-387">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-388">Az.Resources</span></span>
* <span data-ttu-id="0eedb-389">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0eedb-390">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-391">Az.Sql</span></span>
* <span data-ttu-id="0eedb-392">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-393">Az.Storage</span></span>
* <span data-ttu-id="0eedb-394">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0eedb-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0eedb-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0eedb-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0eedb-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0eedb-397">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0eedb-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="0eedb-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0eedb-399">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0eedb-400">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="0eedb-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0eedb-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0eedb-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0eedb-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0eedb-403">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0eedb-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0eedb-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0eedb-405">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0eedb-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0eedb-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0eedb-407">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eedb-408">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0eedb-408">Highlights since the last major release</span></span>
* <span data-ttu-id="0eedb-409">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0eedb-410">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-411">Az.Compute</span></span>
* <span data-ttu-id="0eedb-412">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="0eedb-412">VM Reapply feature</span></span>
    - <span data-ttu-id="0eedb-413">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="0eedb-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0eedb-414">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="0eedb-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0eedb-415">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0eedb-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0eedb-416">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0eedb-417">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0eedb-418">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0eedb-419">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0eedb-420">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0eedb-421">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0eedb-422">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0eedb-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0eedb-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0eedb-424">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0eedb-425">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="0eedb-425">Get the Order</span></span>
* <span data-ttu-id="0eedb-426">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0eedb-427">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="0eedb-427">Create new Order</span></span>
* <span data-ttu-id="0eedb-428">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0eedb-429">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="0eedb-429">Remove the Order</span></span>
* <span data-ttu-id="0eedb-430">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="0eedb-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0eedb-431">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0eedb-431">Now creates Local Share</span></span>
* <span data-ttu-id="0eedb-432">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0eedb-433">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="0eedb-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0eedb-434">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0eedb-435">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="0eedb-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0eedb-436">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0eedb-437">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="0eedb-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="0eedb-438">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0eedb-439">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="0eedb-439">Create new Triggers</span></span>
* <span data-ttu-id="0eedb-440">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0eedb-441">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="0eedb-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-442">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-443">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0eedb-444">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-446">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eedb-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-447">Az.EventHub</span></span>
* <span data-ttu-id="0eedb-448">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0eedb-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eedb-449">Az.FrontDoor</span></span>
* <span data-ttu-id="0eedb-450">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0eedb-451">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0eedb-452">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0eedb-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0eedb-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-454">Az.Network</span></span>
* <span data-ttu-id="0eedb-455">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0eedb-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0eedb-456">Az.PrivateDns</span></span>
* <span data-ttu-id="0eedb-457">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-459">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0eedb-460">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0eedb-461">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0eedb-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0eedb-462">Az.RedisCache</span></span>
* <span data-ttu-id="0eedb-463">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0eedb-464">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0eedb-465">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-466">Az.Resources</span></span>
- <span data-ttu-id="0eedb-467">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0eedb-468">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="0eedb-469">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0eedb-470">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0eedb-471">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-472">Az.Sql</span></span>
* <span data-ttu-id="0eedb-473">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0eedb-474">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0eedb-475">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0eedb-476">Genel</span><span class="sxs-lookup"><span data-stu-id="0eedb-476">General</span></span>
* <span data-ttu-id="0eedb-477">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-478">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-479">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0eedb-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0eedb-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0eedb-480">Az.Advisor</span></span>
* <span data-ttu-id="0eedb-481">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0eedb-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eedb-482">Az.Batch</span></span>
* <span data-ttu-id="0eedb-483">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0eedb-484">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="0eedb-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0eedb-485">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0eedb-486">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0eedb-487">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="0eedb-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0eedb-488">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0eedb-489">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="0eedb-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0eedb-490">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0eedb-491">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0eedb-492">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0eedb-493">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0eedb-494">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0eedb-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0eedb-495">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0eedb-496">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0eedb-497">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0eedb-498">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0eedb-499">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0eedb-500">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0eedb-501">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0eedb-502">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="0eedb-503">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0eedb-504">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0eedb-505">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0eedb-506">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="0eedb-507">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0eedb-508">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="0eedb-509">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0eedb-510">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0eedb-511">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0eedb-512">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0eedb-513">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0eedb-514">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0eedb-515">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0eedb-516">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0eedb-517">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="0eedb-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0eedb-518">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="0eedb-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eedb-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eedb-519">Az.Cdn</span></span>
* <span data-ttu-id="0eedb-520">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0eedb-521">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-522">Az.Compute</span></span>
* <span data-ttu-id="0eedb-523">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="0eedb-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0eedb-524">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0eedb-525">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="0eedb-525">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="0eedb-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0eedb-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0eedb-527">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-527">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0eedb-528">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-528">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0eedb-529">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="0eedb-529">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0eedb-530">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-530">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0eedb-531">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0eedb-531">Breaking changes</span></span>
    - <span data-ttu-id="0eedb-532">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-532">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0eedb-533">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="0eedb-533">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-534">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-535">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-535">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-537">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-537">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0eedb-538">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="0eedb-538">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0eedb-539">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="0eedb-539">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0eedb-540">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="0eedb-540">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0eedb-541">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="0eedb-541">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0eedb-542">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="0eedb-542">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0eedb-543">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eedb-543">Az.FrontDoor</span></span>
* <span data-ttu-id="0eedb-544">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-544">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0eedb-545">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0eedb-545">Az.HDInsight</span></span>
* <span data-ttu-id="0eedb-546">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-546">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0eedb-547">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-547">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0eedb-548">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-548">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0eedb-549">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="0eedb-549">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0eedb-550">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0eedb-550">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0eedb-551">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0eedb-551">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0eedb-552">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0eedb-552">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0eedb-553">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0eedb-553">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0eedb-554">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0eedb-554">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0eedb-555">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-555">Added three cmdlets:</span></span>
    - <span data-ttu-id="0eedb-556">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="0eedb-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0eedb-557">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="0eedb-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0eedb-558">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="0eedb-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0eedb-559">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-559">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0eedb-560">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-560">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0eedb-561">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-561">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0eedb-562">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-562">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0eedb-563">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-563">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0eedb-564">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-564">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0eedb-565">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-565">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0eedb-566">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-566">Added some scenario test cases.</span></span>
* <span data-ttu-id="0eedb-567">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="0eedb-567">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-568">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-569">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="0eedb-569">Breaking changes:</span></span>
    - <span data-ttu-id="0eedb-570">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-570">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0eedb-571">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-571">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0eedb-572">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-572">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0eedb-573">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-573">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0eedb-574">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0eedb-575">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-575">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0eedb-576">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-576">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0eedb-577">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-577">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0eedb-578">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-578">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0eedb-579">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-579">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0eedb-580">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-580">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0eedb-581">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-581">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-582">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-583">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-583">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0eedb-584">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-584">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0eedb-585">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-585">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0eedb-586">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-586">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0eedb-587">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-587">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0eedb-588">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-588">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0eedb-589">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-589">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0eedb-590">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-590">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0eedb-591">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-591">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-592">Az.Resources</span></span>
* <span data-ttu-id="0eedb-593">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-593">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-594">Az.Network</span></span>
* <span data-ttu-id="0eedb-595">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-595">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0eedb-596">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="0eedb-597">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-597">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-598">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-598">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-599">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-599">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-600">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-600">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-601">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-601">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0eedb-602">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-602">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0eedb-603">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0eedb-603">New cmdlet:</span></span>
        - <span data-ttu-id="0eedb-604">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0eedb-604">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0eedb-605">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-605">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0eedb-606">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-606">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0eedb-607">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-607">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0eedb-608">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-608">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0eedb-609">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-609">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0eedb-610">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-610">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0eedb-611">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-611">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0eedb-612">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-612">New cmdlets added:</span></span>
        - <span data-ttu-id="0eedb-613">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0eedb-613">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0eedb-614">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-614">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0eedb-615">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-615">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0eedb-616">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-616">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0eedb-617">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-617">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0eedb-618">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-618">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0eedb-619">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0eedb-620">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-620">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0eedb-621">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-621">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0eedb-622">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-622">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0eedb-623">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-623">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0eedb-624">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-624">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0eedb-625">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-625">New cmdlets added:</span></span>
        - <span data-ttu-id="0eedb-626">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-626">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0eedb-627">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-627">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0eedb-628">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-628">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0eedb-629">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-629">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0eedb-630">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-630">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0eedb-631">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-631">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0eedb-632">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-632">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0eedb-633">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-633">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0eedb-634">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-634">New cmdlets added:</span></span>
        - <span data-ttu-id="0eedb-635">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0eedb-635">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0eedb-636">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0eedb-636">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0eedb-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0eedb-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0eedb-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0eedb-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0eedb-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0eedb-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0eedb-641">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-641">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0eedb-642">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-642">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0eedb-643">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-643">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0eedb-644">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-644">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0eedb-645">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-645">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0eedb-646">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-646">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0eedb-647">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-647">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0eedb-648">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-648">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0eedb-649">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-649">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0eedb-650">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0eedb-650">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0eedb-651">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-651">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0eedb-652">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-652">New cmdlets added:</span></span>
        - <span data-ttu-id="0eedb-653">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0eedb-653">New-AzIpGroup</span></span>
        - <span data-ttu-id="0eedb-654">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0eedb-654">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0eedb-655">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0eedb-655">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0eedb-656">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0eedb-656">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eedb-657">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-657">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-658">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-658">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-659">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-659">Az.Sql</span></span>
* <span data-ttu-id="0eedb-660">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-660">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0eedb-661">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-661">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0eedb-662">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="0eedb-662">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0eedb-663">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="0eedb-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0eedb-664">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="0eedb-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0eedb-665">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-665">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0eedb-666">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-666">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0eedb-667">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-667">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="0eedb-668">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-668">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-669">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-669">Az.Storage</span></span>
* <span data-ttu-id="0eedb-670">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-670">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0eedb-671">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-671">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0eedb-672">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-672">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0eedb-673">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="0eedb-673">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0eedb-674">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0eedb-674">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0eedb-675">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0eedb-675">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="0eedb-676">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-676">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0eedb-677">Genel</span><span class="sxs-lookup"><span data-stu-id="0eedb-677">General</span></span>
* <span data-ttu-id="0eedb-678">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="0eedb-678">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-679">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-679">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-680">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-680">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0eedb-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-681">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-682">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-682">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0eedb-683">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-683">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-684">Az.Automation</span></span>
* <span data-ttu-id="0eedb-685">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-685">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="0eedb-686">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eedb-686">Az.Batch</span></span>
* <span data-ttu-id="0eedb-687">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="0eedb-687">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-688">Az.Compute</span></span>
* <span data-ttu-id="0eedb-689">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-689">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0eedb-690">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-690">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0eedb-691">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-691">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="0eedb-692">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-692">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-693">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-693">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-694">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="0eedb-694">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0eedb-695">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="0eedb-695">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0eedb-696">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-696">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-697">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-697">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-698">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-698">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0eedb-699">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0eedb-699">Az.HealthcareApis</span></span>
* <span data-ttu-id="0eedb-700">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-700">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0eedb-701">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-701">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0eedb-702">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-702">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0eedb-703">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-703">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-704">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-705">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="0eedb-705">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0eedb-706">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-706">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-707">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-708">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-708">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0eedb-709">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0eedb-709">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0eedb-710">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="0eedb-710">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0eedb-711">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-711">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-712">Az.Network</span></span>
* <span data-ttu-id="0eedb-713">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-713">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0eedb-714">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-714">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0eedb-715">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-715">New cmdlets added:</span></span>
        - <span data-ttu-id="0eedb-716">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-716">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0eedb-717">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-717">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0eedb-718">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-718">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0eedb-719">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-719">Updated cmdlets:</span></span>
        - <span data-ttu-id="0eedb-720">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-720">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0eedb-721">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-721">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0eedb-722">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-722">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0eedb-723">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-723">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0eedb-724">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="0eedb-724">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0eedb-725">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="0eedb-725">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0eedb-726">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="0eedb-726">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0eedb-727">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0eedb-727">Az.RedisCache</span></span>
* <span data-ttu-id="0eedb-728">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-728">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-729">Az.Sql</span></span>
* <span data-ttu-id="0eedb-730">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-730">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-731">Az.Storage</span></span>
* <span data-ttu-id="0eedb-732">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-732">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0eedb-733">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="0eedb-733">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0eedb-734">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0eedb-734">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0eedb-735">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="0eedb-735">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0eedb-736">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-736">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0eedb-737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0eedb-737">Az.StorageSync</span></span>
* <span data-ttu-id="0eedb-738">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-738">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-739">Az.Websites</span></span>
* <span data-ttu-id="0eedb-740">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-740">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0eedb-741">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-741">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0eedb-742">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-742">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-743">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-743">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0eedb-744">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-744">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0eedb-745">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="0eedb-745">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-746">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-746">Az.Automation</span></span>
* <span data-ttu-id="0eedb-747">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-747">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0eedb-748">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-748">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0eedb-749">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-749">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-750">Az.Compute</span></span>
* <span data-ttu-id="0eedb-751">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-751">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0eedb-752">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-752">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0eedb-753">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-753">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0eedb-754">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-754">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0eedb-755">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-755">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0eedb-756">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-756">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0eedb-757">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-757">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0eedb-758">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-758">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0eedb-759">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-759">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-760">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-760">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-761">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0eedb-761">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0eedb-762">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-762">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0eedb-763">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0eedb-763">Az.HDInsight</span></span>
* <span data-ttu-id="0eedb-764">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="0eedb-764">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-765">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-765">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-766">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-766">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0eedb-767">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-767">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0eedb-768">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0eedb-768">New cmdlets are:</span></span>
    - <span data-ttu-id="0eedb-769">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0eedb-769">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0eedb-770">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0eedb-770">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0eedb-771">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0eedb-771">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0eedb-772">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0eedb-772">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-773">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-774">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="0eedb-774">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0eedb-775">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-775">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0eedb-776">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="0eedb-776">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0eedb-777">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="0eedb-777">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="0eedb-778">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-778">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0eedb-779">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-779">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0eedb-780">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-780">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0eedb-781">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-781">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0eedb-782">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-782">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0eedb-783">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="0eedb-783">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0eedb-784">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-784">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0eedb-785">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="0eedb-785">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0eedb-786">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-786">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0eedb-787">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="0eedb-787">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0eedb-788">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="0eedb-788">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0eedb-789">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="0eedb-789">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0eedb-790">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="0eedb-790">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0eedb-791">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="0eedb-791">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0eedb-792">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-792">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0eedb-793">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-793">Overall improved help files</span></span>
* <span data-ttu-id="0eedb-794">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-794">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-795">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-795">Az.Network</span></span>
* <span data-ttu-id="0eedb-796">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-796">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="0eedb-797">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-797">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0eedb-798">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-798">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0eedb-799">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-799">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0eedb-800">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-800">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0eedb-801">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-801">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0eedb-802">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-802">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0eedb-803">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-803">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0eedb-804">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-804">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0eedb-805">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-805">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0eedb-806">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-806">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0eedb-807">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-807">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0eedb-808">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-808">New cmdlets</span></span>
        - <span data-ttu-id="0eedb-809">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="0eedb-809">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0eedb-810">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-810">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0eedb-811">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-811">Updated cmdlet:</span></span>
        - <span data-ttu-id="0eedb-812">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0eedb-812">New-VpnSite</span></span>
        - <span data-ttu-id="0eedb-813">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0eedb-813">Update-VpnSite</span></span>
        - <span data-ttu-id="0eedb-814">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-814">New-VpnConnection</span></span>
        - <span data-ttu-id="0eedb-815">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-815">Update-VpnConnection</span></span>
* <span data-ttu-id="0eedb-816">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-816">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-817">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-817">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-818">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-818">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0eedb-819">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-819">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-820">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-820">Az.Resources</span></span>
* <span data-ttu-id="0eedb-821">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-821">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eedb-822">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-822">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-823">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-823">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0eedb-824">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="0eedb-824">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0eedb-825">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0eedb-825">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0eedb-826">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0eedb-826">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0eedb-827">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0eedb-827">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0eedb-828">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0eedb-828">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0eedb-829">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0eedb-829">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0eedb-830">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0eedb-830">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0eedb-831">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0eedb-831">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0eedb-832">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0eedb-832">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0eedb-833">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0eedb-833">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0eedb-834">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0eedb-834">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0eedb-835">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0eedb-835">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0eedb-836">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0eedb-836">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0eedb-837">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="0eedb-837">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0eedb-838">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-838">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0eedb-839">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0eedb-839">Az.SignalR</span></span>
* <span data-ttu-id="0eedb-840">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-840">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-841">Az.Sql</span></span>
* <span data-ttu-id="0eedb-842">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-842">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0eedb-843">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-843">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0eedb-844">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-844">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0eedb-845">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-845">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0eedb-846">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-846">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-847">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-847">Az.Storage</span></span>
* <span data-ttu-id="0eedb-848">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-848">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0eedb-849">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-849">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0eedb-850">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-850">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0eedb-851">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-851">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0eedb-852">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-852">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0eedb-853">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-853">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0eedb-854">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-854">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0eedb-855">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0eedb-855">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0eedb-856">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0eedb-856">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0eedb-857">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0eedb-857">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0eedb-858">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0eedb-858">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-859">Az.Websites</span></span>
* <span data-ttu-id="0eedb-860">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-860">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0eedb-861">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-861">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0eedb-862">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-862">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0eedb-863">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-863">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0eedb-864">Genel</span><span class="sxs-lookup"><span data-stu-id="0eedb-864">General</span></span>
* <span data-ttu-id="0eedb-865">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-865">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-866">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-866">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-867">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="0eedb-867">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0eedb-868">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0eedb-868">Az.Aks</span></span>
* <span data-ttu-id="0eedb-869">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-869">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0eedb-870">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="0eedb-870">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0eedb-871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-871">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-872">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-872">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0eedb-873">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-873">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0eedb-874">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-874">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0eedb-875">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="0eedb-875">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0eedb-876">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-876">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0eedb-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eedb-877">Az.Batch</span></span>
* <span data-ttu-id="0eedb-878">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-878">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eedb-879">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eedb-879">Az.Cdn</span></span>
* <span data-ttu-id="0eedb-880">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-880">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-881">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-881">Az.Compute</span></span>
* <span data-ttu-id="0eedb-882">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-882">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0eedb-883">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-883">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0eedb-884">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-884">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0eedb-885">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-885">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0eedb-886">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0eedb-886">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0eedb-887">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-887">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0eedb-888">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-888">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0eedb-889">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-889">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-890">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-891">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-891">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0eedb-892">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-892">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0eedb-893">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-893">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0eedb-894">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-894">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-895">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-895">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-896">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-896">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eedb-897">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-897">Az.EventHub</span></span>
* <span data-ttu-id="0eedb-898">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="0eedb-898">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0eedb-899">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="0eedb-899">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0eedb-900">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-900">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0eedb-901">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="0eedb-901">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0eedb-902">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0eedb-902">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0eedb-903">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-903">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-904">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-904">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-905">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-905">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-906">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-906">Az.Network</span></span>
* <span data-ttu-id="0eedb-907">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-907">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0eedb-908">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-908">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0eedb-909">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-909">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0eedb-910">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="0eedb-910">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0eedb-911">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-911">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="0eedb-912">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-912">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0eedb-913">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-913">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eedb-914">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-914">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eedb-915">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-915">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0eedb-916">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-916">Added example</span></span>
    - <span data-ttu-id="0eedb-917">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-917">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0eedb-918">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-918">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0eedb-919">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-919">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-920">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-921">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-921">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-922">Az.Resources</span></span>
* <span data-ttu-id="0eedb-923">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-923">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0eedb-924">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-924">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0eedb-925">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="0eedb-925">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0eedb-926">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-926">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0eedb-927">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0eedb-927">Az.ServiceBus</span></span>
* <span data-ttu-id="0eedb-928">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="0eedb-928">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0eedb-929">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="0eedb-929">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0eedb-930">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-930">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="0eedb-931">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-931">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-932">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-932">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0eedb-933">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="0eedb-933">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0eedb-934">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="0eedb-934">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0eedb-935">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-935">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0eedb-936">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="0eedb-936">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0eedb-937">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-937">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-938">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-938">Az.Sql</span></span>
* <span data-ttu-id="0eedb-939">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-939">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-940">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-940">Az.Storage</span></span>
* <span data-ttu-id="0eedb-941">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-941">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0eedb-942">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="0eedb-942">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0eedb-943">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-943">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0eedb-944">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0eedb-944">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0eedb-945">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-945">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0eedb-946">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0eedb-946">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-947">Az.Websites</span></span>
* <span data-ttu-id="0eedb-948">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-948">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0eedb-949">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-949">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-950">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-950">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-951">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-951">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0eedb-952">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-952">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0eedb-953">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-953">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="0eedb-954">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-954">Az.Automation</span></span>
* <span data-ttu-id="0eedb-955">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-955">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eedb-956">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-956">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eedb-957">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-957">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-958">Az.Compute</span></span>
* <span data-ttu-id="0eedb-959">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-959">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0eedb-960">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0eedb-960">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0eedb-961">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-961">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0eedb-962">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="0eedb-962">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-963">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-964">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-964">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0eedb-965">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-965">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eedb-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-966">Az.EventHub</span></span>
* <span data-ttu-id="0eedb-967">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0eedb-967">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0eedb-968">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-968">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-969">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-969">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-970">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-970">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0eedb-971">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0eedb-971">Az.LogicApp</span></span>
* <span data-ttu-id="0eedb-972">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="0eedb-972">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0eedb-973">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-973">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0eedb-974">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-974">Az.ManagedServices</span></span>
* <span data-ttu-id="0eedb-975">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="0eedb-975">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-976">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-976">Az.Network</span></span>
* <span data-ttu-id="0eedb-977">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-977">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0eedb-978">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-978">New cmdlets</span></span>
        - <span data-ttu-id="0eedb-979">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0eedb-979">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0eedb-980">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0eedb-980">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0eedb-981">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-981">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-982">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-982">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-983">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-983">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-984">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-984">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0eedb-985">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="0eedb-985">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0eedb-986">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0eedb-986">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0eedb-987">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="0eedb-987">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0eedb-988">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-988">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0eedb-989">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-989">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0eedb-990">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-990">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0eedb-991">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-991">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0eedb-992">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-992">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0eedb-993">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-993">Updated cmdlets</span></span>
        - <span data-ttu-id="0eedb-994">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-994">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0eedb-995">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-995">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0eedb-996">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-996">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0eedb-997">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-997">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0eedb-998">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-998">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0eedb-999">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-999">Updated cmdlet:</span></span>
        - <span data-ttu-id="0eedb-1000">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-1000">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0eedb-1001">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-1001">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0eedb-1002">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-1002">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0eedb-1003">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1003">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0eedb-1004">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1004">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0eedb-1005">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1005">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eedb-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eedb-1007">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1007">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="0eedb-1008">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1008">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1009">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1009">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1010">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1010">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0eedb-1011">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1011">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0eedb-1012">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1012">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0eedb-1013">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1013">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0eedb-1014">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1014">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0eedb-1015">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1015">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0eedb-1016">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1016">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0eedb-1017">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1017">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0eedb-1018">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1018">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0eedb-1019">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1019">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1020">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1020">Az.Resources</span></span>
- <span data-ttu-id="0eedb-1021">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1021">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0eedb-1022">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1022">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0eedb-1023">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0eedb-1023">Az.ServiceBus</span></span>
* <span data-ttu-id="0eedb-1024">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0eedb-1024">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0eedb-1025">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1025">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1026">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1027">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1027">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0eedb-1028">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1028">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0eedb-1029">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1029">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1030">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1031">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1031">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0eedb-1032">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0eedb-1032">Az.StorageSync</span></span>
* <span data-ttu-id="0eedb-1033">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1033">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0eedb-1034">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1034">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1035">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1035">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1036">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1036">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0eedb-1037">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1037">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0eedb-1038">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1038">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0eedb-1039">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1039">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1040">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1041">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1041">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0eedb-1042">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1042">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0eedb-1043">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1043">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0eedb-1044">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1044">Az.Advisor</span></span>
* <span data-ttu-id="0eedb-1045">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1045">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0eedb-1046">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="0eedb-1046">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0eedb-1047">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-1047">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-1048">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1048">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0eedb-1049">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0eedb-1049">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0eedb-1050">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1050">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0eedb-1051">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="0eedb-1051">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0eedb-1052">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="0eedb-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0eedb-1053">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0eedb-1053">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0eedb-1054">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1054">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-1055">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1055">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1056">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1056">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1057">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1058">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1058">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-1059">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-1060">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1060">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0eedb-1061">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0eedb-1061">Az.EventGrid</span></span>
* <span data-ttu-id="0eedb-1062">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1062">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-1063">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-1063">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-1064">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1064">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1065">Az.Network</span></span>
* <span data-ttu-id="0eedb-1066">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1066">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0eedb-1067">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1067">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0eedb-1068">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1068">Az.PolicyInsights</span></span>
* <span data-ttu-id="0eedb-1069">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1069">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0eedb-1070">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="0eedb-1070">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eedb-1071">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1071">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eedb-1072">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1072">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1073">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1073">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1074">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1074">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1075">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1075">Az.Resources</span></span>
    - <span data-ttu-id="0eedb-1076">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1076">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0eedb-1077">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1077">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0eedb-1078">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1078">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0eedb-1079">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1079">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0eedb-1080">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0eedb-1080">Az.ServiceBus</span></span>
* <span data-ttu-id="0eedb-1081">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1081">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1082">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1082">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1083">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1083">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0eedb-1084">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1084">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0eedb-1085">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0eedb-1085">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0eedb-1086">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0eedb-1086">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0eedb-1087">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0eedb-1087">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0eedb-1088">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0eedb-1088">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0eedb-1089">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0eedb-1089">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0eedb-1090">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0eedb-1090">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0eedb-1091">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1091">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1092">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1093">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1093">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0eedb-1094">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0eedb-1094">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0eedb-1095">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1095">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0eedb-1096">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1096">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0eedb-1097">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1097">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0eedb-1098">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1098">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0eedb-1099">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1099">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0eedb-1100">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1100">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0eedb-1101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0eedb-1101">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0eedb-1102">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0eedb-1102">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0eedb-1103">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0eedb-1103">Az.StorageSync</span></span>
* <span data-ttu-id="0eedb-1104">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="0eedb-1104">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0eedb-1105">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1105">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1106">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1107">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1107">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0eedb-1108">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0eedb-1108">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0eedb-1109">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1109">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0eedb-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0eedb-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0eedb-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0eedb-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1112">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1113">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1113">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0eedb-1114">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1114">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0eedb-1115">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0eedb-1115">Az.Dns</span></span>
* <span data-ttu-id="0eedb-1116">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1116">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0eedb-1117">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0eedb-1117">Az.EventGrid</span></span>
* <span data-ttu-id="0eedb-1118">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1118">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0eedb-1119">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1119">New cmdlets:</span></span>
    - <span data-ttu-id="0eedb-1120">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0eedb-1120">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0eedb-1121">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1121">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0eedb-1122">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0eedb-1122">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0eedb-1123">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1123">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0eedb-1124">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0eedb-1124">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0eedb-1125">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1125">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0eedb-1126">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0eedb-1126">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0eedb-1127">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1127">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0eedb-1128">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0eedb-1128">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0eedb-1129">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1129">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0eedb-1130">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1130">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0eedb-1131">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1131">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0eedb-1132">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0eedb-1132">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0eedb-1133">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1133">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="0eedb-1134">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1134">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0eedb-1135">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1135">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0eedb-1136">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1136">Updated cmdlets:</span></span>
    - <span data-ttu-id="0eedb-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0eedb-1138">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1138">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0eedb-1139">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1139">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0eedb-1140">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1140">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0eedb-1141">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1141">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0eedb-1142">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="0eedb-1142">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0eedb-1143">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1143">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0eedb-1144">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1144">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0eedb-1145">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="0eedb-1145">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="0eedb-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0eedb-1147">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1147">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0eedb-1148">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0eedb-1148">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0eedb-1149">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1149">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0eedb-1150">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1150">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0eedb-1151">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1151">Az.FrontDoor</span></span>
* <span data-ttu-id="0eedb-1152">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0eedb-1152">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0eedb-1153">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1153">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0eedb-1154">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0eedb-1154">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0eedb-1155">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1155">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1156">Az.Network</span></span>
* <span data-ttu-id="0eedb-1157">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1157">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0eedb-1158">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1158">New cmdlets</span></span>
        - <span data-ttu-id="0eedb-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0eedb-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0eedb-1160">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1160">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0eedb-1161">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1161">New cmdlets</span></span> 
        - <span data-ttu-id="0eedb-1162">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0eedb-1162">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0eedb-1163">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1163">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0eedb-1164">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1164">New cmdlets</span></span> 
        - <span data-ttu-id="0eedb-1165">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0eedb-1165">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="0eedb-1166">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0eedb-1166">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0eedb-1167">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0eedb-1167">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0eedb-1168">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-1168">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0eedb-1169">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-1169">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0eedb-1170">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1170">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0eedb-1171">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1171">New cmdlets</span></span>
        - <span data-ttu-id="0eedb-1172">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0eedb-1172">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0eedb-1173">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0eedb-1173">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0eedb-1174">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0eedb-1174">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0eedb-1175">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0eedb-1175">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0eedb-1176">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1176">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0eedb-1177">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1177">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0eedb-1178">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1178">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0eedb-1179">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1179">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0eedb-1180">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1180">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0eedb-1181">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1181">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0eedb-1182">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1182">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0eedb-1183">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1183">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0eedb-1184">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1184">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0eedb-1185">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1185">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0eedb-1186">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1186">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0eedb-1187">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1187">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0eedb-1188">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1188">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0eedb-1189">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1189">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0eedb-1190">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1190">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0eedb-1191">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1191">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0eedb-1192">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1192">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0eedb-1193">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0eedb-1193">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0eedb-1194">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0eedb-1194">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="0eedb-1195">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1195">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="0eedb-1196">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1196">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0eedb-1197">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1197">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0eedb-1198">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1198">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eedb-1199">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1199">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eedb-1200">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1200">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1201">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1201">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1202">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="0eedb-1202">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0eedb-1203">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1203">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0eedb-1204">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1204">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0eedb-1205">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1205">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eedb-1206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-1206">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-1207">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1207">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1208">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1208">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1209">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1209">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0eedb-1210">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1210">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0eedb-1211">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1211">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0eedb-1212">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0eedb-1212">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0eedb-1213">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0eedb-1213">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0eedb-1214">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0eedb-1214">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0eedb-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0eedb-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0eedb-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0eedb-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1217">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1218">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="0eedb-1218">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0eedb-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1219">New-AzStorageAccount</span></span>
* <span data-ttu-id="0eedb-1220">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1220">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0eedb-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1222">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1222">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1223">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="0eedb-1223">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0eedb-1224">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1224">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0eedb-1225">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1225">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0eedb-1226">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eedb-1226">Az.Cdn</span></span>
* <span data-ttu-id="0eedb-1227">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1227">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1228">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1229">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1229">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0eedb-1230">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0eedb-1230">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eedb-1231">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-1231">Az.EventHub</span></span>
* <span data-ttu-id="0eedb-1232">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1232">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0eedb-1233">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1233">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1234">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1234">Az.Network</span></span>
* <span data-ttu-id="0eedb-1235">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1235">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0eedb-1236">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1236">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0eedb-1237">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1237">Az.PolicyInsights</span></span>
* <span data-ttu-id="0eedb-1238">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1238">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1239">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1239">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1240">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1240">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0eedb-1241">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0eedb-1241">Az.ServiceBus</span></span>
* <span data-ttu-id="0eedb-1242">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1242">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eedb-1243">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-1243">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-1244">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1244">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0eedb-1245">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1245">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1246">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1247">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1247">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0eedb-1248">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1248">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0eedb-1249">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1249">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0eedb-1250">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1250">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1251">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1252">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1252">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0eedb-1253">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1253">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0eedb-1254">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-1254">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-1255">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1255">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0eedb-1256">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1256">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0eedb-1257">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="0eedb-1257">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0eedb-1258">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0eedb-1258">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0eedb-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0eedb-1260">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0eedb-1260">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0eedb-1261">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1261">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0eedb-1262">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="0eedb-1262">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0eedb-1263">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1263">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0eedb-1264">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1264">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0eedb-1265">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="0eedb-1265">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0eedb-1266">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1266">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0eedb-1267">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="0eedb-1267">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0eedb-1268">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1268">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0eedb-1269">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="0eedb-1269">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0eedb-1270">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1270">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0eedb-1271">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1271">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0eedb-1272">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="0eedb-1272">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0eedb-1273">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1273">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="0eedb-1274">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="0eedb-1274">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0eedb-1275">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1275">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0eedb-1276">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1276">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0eedb-1277">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1277">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0eedb-1278">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1278">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="0eedb-1279">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1279">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0eedb-1280">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1280">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0eedb-1281">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1281">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0eedb-1282">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1282">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0eedb-1283">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1283">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0eedb-1284">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1284">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0eedb-1285">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1285">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="0eedb-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0eedb-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0eedb-1287">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1287">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0eedb-1288">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1288">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0eedb-1289">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1289">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0eedb-1290">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1290">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0eedb-1291">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1291">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0eedb-1292">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1292">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0eedb-1293">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1293">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0eedb-1294">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1294">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="0eedb-1295">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1295">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0eedb-1296">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1296">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0eedb-1297">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1297">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0eedb-1298">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0eedb-1299">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1299">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0eedb-1300">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1300">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0eedb-1301">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1301">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="0eedb-1302">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1302">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0eedb-1303">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1303">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0eedb-1304">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1304">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0eedb-1305">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1305">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0eedb-1306">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1306">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0eedb-1307">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1307">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0eedb-1308">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1308">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0eedb-1309">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1309">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0eedb-1310">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1310">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0eedb-1311">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1311">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0eedb-1312">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0eedb-1313">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0eedb-1314">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0eedb-1315">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1315">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0eedb-1316">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1316">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0eedb-1317">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="0eedb-1317">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0eedb-1318">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1318">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0eedb-1319">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1319">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0eedb-1320">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1320">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0eedb-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0eedb-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0eedb-1322">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1322">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0eedb-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0eedb-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0eedb-1324">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1324">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0eedb-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0eedb-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0eedb-1326">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1326">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0eedb-1327">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1327">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0eedb-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0eedb-1329">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1329">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="0eedb-1330">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1330">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0eedb-1331">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="0eedb-1331">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-1332">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1332">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1333">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1333">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0eedb-1334">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0eedb-1335">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1335">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0eedb-1336">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1336">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0eedb-1337">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1337">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0eedb-1338">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1338">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0eedb-1339">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1339">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1340">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1341">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1341">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0eedb-1342">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1342">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-1343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-1343">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-1344">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1344">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-1345">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1345">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-1346">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1346">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1347">Az.Network</span></span>
* <span data-ttu-id="0eedb-1348">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1348">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0eedb-1349">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1349">Updated cmdlet:</span></span>
        - <span data-ttu-id="0eedb-1350">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-1350">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0eedb-1351">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1351">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1352">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1353">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1353">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1354">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1354">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1355">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1355">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0eedb-1356">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1356">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1357">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1358">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="0eedb-1358">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eedb-1359">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1359">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eedb-1360">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1360">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0eedb-1361">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1361">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1362">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1363">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1363">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0eedb-1364">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0eedb-1364">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0eedb-1365">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-1365">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0eedb-1366">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1366">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0eedb-1367">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1367">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0eedb-1368">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1368">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="0eedb-1369">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1369">Breaking changes</span></span>
    - <span data-ttu-id="0eedb-1370">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1370">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0eedb-1371">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1371">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0eedb-1372">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0eedb-1372">Az.DeploymentManager</span></span>
* <span data-ttu-id="0eedb-1373">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1373">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0eedb-1374">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0eedb-1374">Az.Dns</span></span>
* <span data-ttu-id="0eedb-1375">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1375">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0eedb-1376">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1376">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0eedb-1377">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1377">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0eedb-1378">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1378">Az.FrontDoor</span></span>
* <span data-ttu-id="0eedb-1379">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1379">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0eedb-1380">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="0eedb-1380">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0eedb-1381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0eedb-1381">Az.HDInsight</span></span>
* <span data-ttu-id="0eedb-1382">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1382">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0eedb-1383">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0eedb-1383">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0eedb-1384">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0eedb-1384">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0eedb-1385">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1385">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0eedb-1386">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1386">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0eedb-1387">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1387">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0eedb-1388">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1388">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-1389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1389">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-1390">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1390">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="0eedb-1391">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0eedb-1391">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0eedb-1392">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0eedb-1392">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0eedb-1393">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0eedb-1393">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0eedb-1394">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1394">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0eedb-1395">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0eedb-1395">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0eedb-1396">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0eedb-1396">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0eedb-1397">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1397">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0eedb-1398">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1398">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0eedb-1399">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1399">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0eedb-1400">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1400">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0eedb-1401">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1401">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0eedb-1402">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1402">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0eedb-1403">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1403">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1404">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1404">Az.Network</span></span>
* <span data-ttu-id="0eedb-1405">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="0eedb-1405">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0eedb-1406">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1406">New cmdlets</span></span>
        - <span data-ttu-id="0eedb-1407">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0eedb-1407">New-AzNatGateway</span></span>
        - <span data-ttu-id="0eedb-1408">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0eedb-1408">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0eedb-1409">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0eedb-1409">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0eedb-1410">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0eedb-1410">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0eedb-1411">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1411">Updated cmdlets</span></span>
        - <span data-ttu-id="0eedb-1412">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0eedb-1412">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0eedb-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0eedb-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0eedb-1414">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1414">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0eedb-1415">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1415">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0eedb-1416">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1416">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0eedb-1417">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1417">Az.PolicyInsights</span></span>
* <span data-ttu-id="0eedb-1418">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1418">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0eedb-1419">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1419">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0eedb-1420">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1420">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1421">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1421">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1422">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1422">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0eedb-1423">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1423">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0eedb-1424">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1424">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0eedb-1425">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1425">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0eedb-1426">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1426">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0eedb-1427">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1427">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0eedb-1428">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0eedb-1428">Az.Relay</span></span>
* <span data-ttu-id="0eedb-1429">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="0eedb-1429">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0eedb-1430">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0eedb-1430">Az.ServiceBus</span></span>
* <span data-ttu-id="0eedb-1431">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1431">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1432">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1433">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1433">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0eedb-1434">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1434">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0eedb-1435">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="0eedb-1435">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0eedb-1436">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1436">New-AzStorageAccount</span></span>
* <span data-ttu-id="0eedb-1437">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="0eedb-1437">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0eedb-1438">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1438">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0eedb-1439">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1439">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0eedb-1440">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1440">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1441">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1442">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1442">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0eedb-1443">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1443">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0eedb-1444">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1444">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eedb-1445">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0eedb-1445">Highlights since the last major release</span></span>
* <span data-ttu-id="0eedb-1446">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1446">General availability of `Az` module</span></span>
* <span data-ttu-id="0eedb-1447">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0eedb-1447">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0eedb-1448">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0eedb-1448">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0eedb-1449">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1449">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0eedb-1450">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1450">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eedb-1451">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1451">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0eedb-1452">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1452">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1453">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1453">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1454">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1454">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0eedb-1455">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eedb-1455">Az.Batch</span></span>
* <span data-ttu-id="0eedb-1456">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eedb-1457">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eedb-1457">Az.Cdn</span></span>
* <span data-ttu-id="0eedb-1458">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1458">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eedb-1459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1459">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eedb-1460">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1460">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1461">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1462">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1462">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0eedb-1463">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1463">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eedb-1464">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1464">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-1465">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-1466">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1466">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-1468">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1468">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0eedb-1469">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0eedb-1469">Az.EventGrid</span></span>
* <span data-ttu-id="0eedb-1470">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1470">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eedb-1471">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-1471">Az.EventHub</span></span>
* <span data-ttu-id="0eedb-1472">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1472">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="0eedb-1473">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0eedb-1473">Az.HDInsight</span></span>
* <span data-ttu-id="0eedb-1474">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-1475">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-1475">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-1476">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1476">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-1477">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-1477">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-1478">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1478">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eedb-1479">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1479">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0eedb-1480">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0eedb-1480">Az.MachineLearning</span></span>
* <span data-ttu-id="0eedb-1481">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1481">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0eedb-1482">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0eedb-1482">Az.Media</span></span>
* <span data-ttu-id="0eedb-1483">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1483">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-1484">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1484">Az.Monitor</span></span>
  * <span data-ttu-id="0eedb-1485">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1485">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0eedb-1486">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0eedb-1486">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0eedb-1487">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0eedb-1487">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0eedb-1488">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0eedb-1488">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0eedb-1489">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0eedb-1489">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0eedb-1490">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0eedb-1490">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0eedb-1491">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1491">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1492">Az.Network</span></span>
* <span data-ttu-id="0eedb-1493">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eedb-1494">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1494">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0eedb-1495">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0eedb-1495">Az.NotificationHubs</span></span>
* <span data-ttu-id="0eedb-1496">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eedb-1497">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1497">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eedb-1498">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0eedb-1499">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0eedb-1499">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0eedb-1500">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1500">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1501">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1502">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1502">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eedb-1503">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1503">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0eedb-1504">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1504">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0eedb-1505">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1505">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0eedb-1506">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0eedb-1506">Az.RedisCache</span></span>
* <span data-ttu-id="0eedb-1507">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1507">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1508">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1509">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1509">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1510">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1511">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1511">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0eedb-1512">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1512">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eedb-1513">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1513">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0eedb-1514">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1514">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0eedb-1515">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1515">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0eedb-1516">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1516">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0eedb-1517">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1517">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1518">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1519">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1519">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0eedb-1520">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0eedb-1521">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1521">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0eedb-1522">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1522">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0eedb-1523">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1523">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eedb-1524">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0eedb-1524">Highlights since the last major release</span></span>
* <span data-ttu-id="0eedb-1525">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1525">General availability of `Az` module</span></span>
* <span data-ttu-id="0eedb-1526">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0eedb-1526">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0eedb-1527">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0eedb-1527">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0eedb-1528">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1528">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0eedb-1529">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1529">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eedb-1530">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1530">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0eedb-1531">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1531">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1532">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1533">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1533">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0eedb-1534">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1534">Az.AnalysisServices</span></span>
* <span data-ttu-id="0eedb-1535">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-1535">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0eedb-1536">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="0eedb-1536">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-1537">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1537">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1538">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1538">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0eedb-1539">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1539">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0eedb-1540">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1540">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1541">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1542">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1542">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0eedb-1543">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1543">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0eedb-1544">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-1544">Az.ContainerInstance</span></span>
* <span data-ttu-id="0eedb-1545">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1545">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-1546">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-1547">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1547">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0eedb-1548">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1548">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1549">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1550">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1550">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0eedb-1551">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1551">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0eedb-1552">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1552">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0eedb-1553">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0eedb-1553">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0eedb-1554">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1554">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0eedb-1555">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0eedb-1555">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1556">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1557">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1557">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1558">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1559">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="0eedb-1559">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0eedb-1560">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0eedb-1560">New-AzStorageContext</span></span>
* <span data-ttu-id="0eedb-1561">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-1561">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0eedb-1562">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0eedb-1562">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0eedb-1563">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0eedb-1563">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0eedb-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0eedb-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0eedb-1566">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-1566">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0eedb-1567">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-1567">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0eedb-1568">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-1568">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0eedb-1569">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-1569">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0eedb-1570">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0eedb-1570">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0eedb-1571">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1571">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0eedb-1572">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="0eedb-1572">Highlights since the last major release</span></span>
* <span data-ttu-id="0eedb-1573">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1573">General availability of `Az` module</span></span>
* <span data-ttu-id="0eedb-1574">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0eedb-1574">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0eedb-1575">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0eedb-1575">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0eedb-1576">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1576">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0eedb-1577">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1577">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eedb-1578">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1578">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0eedb-1579">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1579">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-1580">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1580">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1581">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1581">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0eedb-1582">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="0eedb-1582">Dynamic grouping</span></span>
    * <span data-ttu-id="0eedb-1583">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="0eedb-1583">Pre-Post script</span></span>
    * <span data-ttu-id="0eedb-1584">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1584">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1585">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1585">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1586">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1586">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0eedb-1587">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1587">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-1588">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-1589">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1589">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1590">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1590">Az.Network</span></span>
* <span data-ttu-id="0eedb-1591">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1591">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0eedb-1592">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1592">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1593">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1593">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1594">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1594">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0eedb-1595">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1595">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1596">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1597">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1597">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0eedb-1598">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1598">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1599">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1599">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1600">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1600">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1601">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1601">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1602">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-1602">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0eedb-1603">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1603">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0eedb-1604">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1604">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0eedb-1605">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1605">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0eedb-1606">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0eedb-1606">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0eedb-1607">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0eedb-1607">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0eedb-1608">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1608">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1609">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1610">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1610">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0eedb-1611">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1611">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1612">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1612">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1613">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1613">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0eedb-1614">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1614">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-1615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1615">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1616">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1616">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0eedb-1617">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1617">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0eedb-1618">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="0eedb-1618">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eedb-1619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eedb-1619">Az.Cdn</span></span>
* <span data-ttu-id="0eedb-1620">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1620">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1621">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1622">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1622">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-1623">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-1623">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-1624">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1624">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0eedb-1625">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0eedb-1625">Az.LogicApp</span></span>
* <span data-ttu-id="0eedb-1626">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="0eedb-1626">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1627">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1627">Az.Network</span></span>
* <span data-ttu-id="0eedb-1628">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1628">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1630">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1630">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0eedb-1631">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1631">SDK Update</span></span>
* <span data-ttu-id="0eedb-1632">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1632">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0eedb-1633">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1633">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1634">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1635">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1635">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0eedb-1636">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0eedb-1636">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0eedb-1637">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1637">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0eedb-1638">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0eedb-1638">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0eedb-1639">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1639">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0eedb-1640">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0eedb-1640">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1641">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1642">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1642">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0eedb-1643">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1643">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1644">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1645">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0eedb-1645">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0eedb-1646">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1646">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0eedb-1647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1647">Az.AnalysisServices</span></span>
* <span data-ttu-id="0eedb-1648">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1648">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1649">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1650">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1650">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0eedb-1651">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1651">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0eedb-1652">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1652">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eedb-1653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1653">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eedb-1654">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1654">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1655">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1656">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1656">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0eedb-1657">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1657">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0eedb-1658">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1658">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0eedb-1659">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1659">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-1660">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-1660">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-1661">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1661">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0eedb-1662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-1662">Az.EventHub</span></span>
* <span data-ttu-id="0eedb-1663">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1663">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-1664">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-1664">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-1665">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1665">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0eedb-1666">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0eedb-1666">Az.LogicApp</span></span>
* <span data-ttu-id="0eedb-1667">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1667">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0eedb-1668">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1668">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0eedb-1669">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1669">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0eedb-1670">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eedb-1670">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0eedb-1671">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eedb-1671">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0eedb-1672">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eedb-1672">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0eedb-1673">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0eedb-1673">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0eedb-1674">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1674">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0eedb-1675">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eedb-1675">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0eedb-1676">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eedb-1676">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0eedb-1677">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eedb-1677">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0eedb-1678">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eedb-1678">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0eedb-1679">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1679">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0eedb-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1680">Az.Monitor</span></span>
* <span data-ttu-id="0eedb-1681">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1681">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1682">Az.Network</span></span>
* <span data-ttu-id="0eedb-1683">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1683">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0eedb-1684">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1684">Az.OperationalInsights</span></span>
* <span data-ttu-id="0eedb-1685">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1685">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0eedb-1686">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1686">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0eedb-1687">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1687">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0eedb-1688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1688">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1689">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0eedb-1690">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0eedb-1691">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1691">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0eedb-1692">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1692">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1693">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1694">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1694">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0eedb-1695">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1695">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1696">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1696">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1697">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1697">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0eedb-1698">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1698">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1699">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1700">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0eedb-1700">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0eedb-1701">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1701">Az.AnalysisServices</span></span>
<span data-ttu-id="0eedb-1702">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1702">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1703">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1704">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1704">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0eedb-1705">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1705">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0eedb-1706">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1706">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1707">Az.RecoveryServices</span></span>
<span data-ttu-id="0eedb-1708">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1708">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1709">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1709">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1710">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1710">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0eedb-1711">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0eedb-1711">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0eedb-1712">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1712">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0eedb-1713">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0eedb-1713">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1714">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0eedb-1716">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1716">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0eedb-1717">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1717">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0eedb-1718">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1718">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1719">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1720">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1720">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0eedb-1721">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1721">Az.AnalysisServices</span></span>
* <span data-ttu-id="0eedb-1722">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="0eedb-1722">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1723">Az.RecoveryServices</span></span>
* <span data-ttu-id="0eedb-1724">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="0eedb-1724">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0eedb-1725">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1725">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1726">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1726">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1727">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1727">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0eedb-1728">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1728">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eedb-1729">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1729">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0eedb-1730">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0eedb-1730">Az.Aks</span></span>
* <span data-ttu-id="0eedb-1731">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1731">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0eedb-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1732">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1733">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1733">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0eedb-1734">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1734">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0eedb-1735">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0eedb-1735">Az.Cdn</span></span>
* <span data-ttu-id="0eedb-1736">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1736">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1737">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1738">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1738">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0eedb-1739">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1739">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0eedb-1740">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1740">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0eedb-1741">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0eedb-1741">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0eedb-1742">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1742">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0eedb-1743">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eedb-1743">Az.DataFactory</span></span>
* <span data-ttu-id="0eedb-1744">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1744">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-1745">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-1745">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-1746">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1746">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0eedb-1747">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0eedb-1747">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0eedb-1748">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1748">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-1749">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-1749">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-1750">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1750">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0eedb-1751">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-1751">Az.KeyVault</span></span>
* <span data-ttu-id="0eedb-1752">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1752">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-1753">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1753">Az.Network</span></span>
* <span data-ttu-id="0eedb-1754">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1754">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1755">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1756">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1756">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0eedb-1757">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1757">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0eedb-1758">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1758">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0eedb-1759">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0eedb-1760">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1760">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0eedb-1761">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1761">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0eedb-1762">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0eedb-1762">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eedb-1763">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-1763">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-1764">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0eedb-1764">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0eedb-1765">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1765">Fix some error messages.</span></span>
* <span data-ttu-id="0eedb-1766">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1766">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0eedb-1767">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1767">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0eedb-1768">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0eedb-1768">Az.SignalR</span></span>
* <span data-ttu-id="0eedb-1769">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1769">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1770">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1771">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1771">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eedb-1772">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1772">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0eedb-1773">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1773">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0eedb-1774">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-1774">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1775">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1776">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1776">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eedb-1777">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1777">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0eedb-1778">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0eedb-1778">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0eedb-1779">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0eedb-1779">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0eedb-1780">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0eedb-1780">Az.TrafficManager</span></span>
* <span data-ttu-id="0eedb-1781">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1781">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1782">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1782">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1783">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1783">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0eedb-1784">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1784">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0eedb-1785">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1785">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0eedb-1786">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="0eedb-1786">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0eedb-1787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1787">Az.Accounts</span></span>
* <span data-ttu-id="0eedb-1788">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1788">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-1789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1789">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1790">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1790">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0eedb-1791">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1791">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0eedb-1792">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1792">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-1793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-1793">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-1794">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1794">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0eedb-1795">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1795">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0eedb-1796">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0eedb-1796">Az.EventGrid</span></span>
* <span data-ttu-id="0eedb-1797">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1797">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0eedb-1798">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1798">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0eedb-1799">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1799">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0eedb-1800">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="0eedb-1800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0eedb-1801">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="0eedb-1801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0eedb-1802">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1802">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0eedb-1803">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1803">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0eedb-1804">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="0eedb-1804">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0eedb-1805">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="0eedb-1805">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0eedb-1806">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1806">Dead letter endpoint.</span></span>
* <span data-ttu-id="0eedb-1807">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1807">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0eedb-1808">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1808">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0eedb-1809">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0eedb-1809">Az.IotHub</span></span>
* <span data-ttu-id="0eedb-1810">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1810">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0eedb-1811">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0eedb-1811">Az.LogicApp</span></span>
* <span data-ttu-id="0eedb-1812">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1812">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-1813">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1813">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1814">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1814">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0eedb-1815">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0eedb-1815">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0eedb-1816">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1816">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0eedb-1817">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1817">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0eedb-1818">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1818">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0eedb-1819">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0eedb-1819">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0eedb-1820">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0eedb-1820">Az.SignalR</span></span>
* <span data-ttu-id="0eedb-1821">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1821">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-1822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1822">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1823">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1823">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0eedb-1824">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1824">Az.Storage</span></span>
* <span data-ttu-id="0eedb-1825">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1825">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0eedb-1826">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0eedb-1826">New-AzStorageContext</span></span>
* <span data-ttu-id="0eedb-1827">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1827">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0eedb-1828">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0eedb-1828">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-1829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1829">Az.Websites</span></span>
* <span data-ttu-id="0eedb-1830">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1830">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0eedb-1831">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0eedb-1831">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0eedb-1832">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="0eedb-1832">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0eedb-1833">Genel</span><span class="sxs-lookup"><span data-stu-id="0eedb-1833">General</span></span>

- <span data-ttu-id="0eedb-1834">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1834">General Availability of Az Module</span></span>
- <span data-ttu-id="0eedb-1835">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="0eedb-1835">Online help for each module</span></span>
- <span data-ttu-id="0eedb-1836">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1836">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0eedb-1837">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1837">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0eedb-1838">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0eedb-1838">Az.Accounts</span></span>
- <span data-ttu-id="0eedb-1839">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eedb-1839">Changed from Az.Profile</span></span>
- <span data-ttu-id="0eedb-1840">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1840">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0eedb-1841">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-1841">Az.ApiManagement</span></span>
- <span data-ttu-id="0eedb-1842">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="0eedb-1842">Fixes for #7002</span></span>
- <span data-ttu-id="0eedb-1843">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0eedb-1844">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0eedb-1844">Az.Batch</span></span>
- <span data-ttu-id="0eedb-1845">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1845">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0eedb-1846">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1846">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0eedb-1847">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1847">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0eedb-1848">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0eedb-1848">Az.Billing</span></span>
- <span data-ttu-id="0eedb-1849">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1849">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0eedb-1850">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1850">Az.CognitivServices</span></span>
- <span data-ttu-id="0eedb-1851">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1851">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0eedb-1852">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1852">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0eedb-1853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-1853">Az.ContainerInstance</span></span>
- <span data-ttu-id="0eedb-1854">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1854">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0eedb-1855">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0eedb-1855">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0eedb-1856">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1856">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-1857">Az.DataLakeStore</span></span>
- <span data-ttu-id="0eedb-1858">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1858">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0eedb-1859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1859">Az.Monitor</span></span>
- <span data-ttu-id="0eedb-1860">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1860">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0eedb-1861">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0eedb-1861">Az.KeyVault</span></span>
- <span data-ttu-id="0eedb-1862">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1862">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0eedb-1863">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0eedb-1863">Az.MachineLearning</span></span>
- <span data-ttu-id="0eedb-1864">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1864">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0eedb-1865">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0eedb-1865">Az.Media</span></span>
- <span data-ttu-id="0eedb-1866">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="0eedb-1866">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0eedb-1867">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1867">Az.Network</span></span>
<span data-ttu-id="0eedb-1868">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1868">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0eedb-1869">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="0eedb-1869">New cmdlets added:</span></span>
        - <span data-ttu-id="0eedb-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eedb-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eedb-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eedb-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eedb-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0eedb-1875">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1875">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0eedb-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0eedb-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0eedb-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eedb-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0eedb-1878">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1878">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0eedb-1879">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0eedb-1879">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0eedb-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0eedb-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0eedb-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0eedb-1882">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-1882">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0eedb-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0eedb-1884">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0eedb-1885">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1885">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0eedb-1886">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0eedb-1886">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0eedb-1887">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0eedb-1887">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0eedb-1888">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0eedb-1888">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0eedb-1889">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1889">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0eedb-1890">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1890">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0eedb-1891">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-1891">Az.OperationalInsights</span></span>
- <span data-ttu-id="0eedb-1892">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0eedb-1893">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eedb-1893">Az.Profile</span></span>
- <span data-ttu-id="0eedb-1894">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1894">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1895">Az.RecoveryServices</span></span>
- <span data-ttu-id="0eedb-1896">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1896">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0eedb-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1897">Az.Resources</span></span>
- <span data-ttu-id="0eedb-1898">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1898">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0eedb-1899">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-1899">Az.ServiceFabric</span></span>
- <span data-ttu-id="0eedb-1900">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="0eedb-1900">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0eedb-1901">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1901">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0eedb-1902">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0eedb-1902">Az.SIgnalR</span></span>
- <span data-ttu-id="0eedb-1903">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1903">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0eedb-1904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1904">Az.Sql</span></span>
- <span data-ttu-id="0eedb-1905">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1905">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0eedb-1906">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1906">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0eedb-1907">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0eedb-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1908">Az.Storage</span></span>
- <span data-ttu-id="0eedb-1909">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0eedb-1910">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1910">Az.Websites</span></span>
- <span data-ttu-id="0eedb-1911">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0eedb-1911">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0eedb-1912">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="0eedb-1912">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0eedb-1913">Genel</span><span class="sxs-lookup"><span data-stu-id="0eedb-1913">General</span></span>

* <span data-ttu-id="0eedb-1914">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1914">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0eedb-1915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1915">Az.Compute</span></span>

* <span data-ttu-id="0eedb-1916">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1916">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-1917">Az.DataLakeStore</span></span>

* <span data-ttu-id="0eedb-1918">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1918">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0eedb-1919">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0eedb-1919">Az.FrontDoor</span></span>

* <span data-ttu-id="0eedb-1920">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1920">Fixed some broken links</span></span>
    - <span data-ttu-id="0eedb-1921">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1921">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0eedb-1922">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1922">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0eedb-1923">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-1923">Az.RecoveryServices</span></span>

* <span data-ttu-id="0eedb-1924">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1924">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0eedb-1925">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1925">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0eedb-1926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1926">Az.Resources</span></span>

* <span data-ttu-id="0eedb-1927">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1927">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0eedb-1928">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1928">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0eedb-1929">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1929">Az.Sql</span></span>

* <span data-ttu-id="0eedb-1930">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0eedb-1930">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0eedb-1931">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1931">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0eedb-1932">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1932">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0eedb-1933">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0eedb-1933">Az.Storage</span></span>

* <span data-ttu-id="0eedb-1934">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1934">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0eedb-1935">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1935">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0eedb-1936">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0eedb-1936">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0eedb-1937">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1937">Support Static Website configuration</span></span>
    - <span data-ttu-id="0eedb-1938">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0eedb-1938">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0eedb-1939">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0eedb-1939">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0eedb-1940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-1940">Az.Websites</span></span>

* <span data-ttu-id="0eedb-1941">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0eedb-1941">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0eedb-1942">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1942">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0eedb-1943">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1943">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0eedb-1944">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="0eedb-1944">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0eedb-1945">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0eedb-1945">Az.ApiManagement</span></span>
* <span data-ttu-id="0eedb-1946">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1946">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0eedb-1947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0eedb-1947">Az.Automation</span></span>
* <span data-ttu-id="0eedb-1948">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="0eedb-1948">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0eedb-1949">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1949">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0eedb-1950">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1950">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0eedb-1951">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1951">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0eedb-1952">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1952">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0eedb-1953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-1953">Az.Compute</span></span>
* <span data-ttu-id="0eedb-1954">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1954">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0eedb-1955">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1955">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0eedb-1956">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-1956">Az.ContainerInstance</span></span>
* <span data-ttu-id="0eedb-1957">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1957">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0eedb-1958">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0eedb-1958">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0eedb-1959">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1959">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0eedb-1960">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-1960">Az.Network</span></span>
* <span data-ttu-id="0eedb-1961">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1961">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0eedb-1962">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1962">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0eedb-1963">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1963">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0eedb-1964">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1964">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0eedb-1965">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0eedb-1965">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0eedb-1966">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1966">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0eedb-1967">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1967">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0eedb-1968">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0eedb-1968">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0eedb-1969">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1969">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0eedb-1970">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="0eedb-1970">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0eedb-1971">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0eedb-1971">Az.Relay</span></span>
* <span data-ttu-id="0eedb-1972">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1972">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0eedb-1973">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-1973">Az.Resources</span></span>
* <span data-ttu-id="0eedb-1974">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1974">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0eedb-1975">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1975">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0eedb-1976">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0eedb-1976">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0eedb-1977">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-1977">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-1978">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1978">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0eedb-1979">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-1979">Az.Sql</span></span>
* <span data-ttu-id="0eedb-1980">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1980">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0eedb-1981">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-1981">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eedb-1982">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-1982">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eedb-1983">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-1983">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eedb-1984">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0eedb-1984">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0eedb-1985">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eedb-1985">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0eedb-1986">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eedb-1986">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0eedb-1987">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eedb-1987">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0eedb-1988">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0eedb-1988">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0eedb-1989">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1989">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0eedb-1990">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1990">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0eedb-1991">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1991">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0eedb-1992">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1992">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0eedb-1993">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1993">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0eedb-1994">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1994">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0eedb-1995">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0eedb-1995">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0eedb-1996">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-1996">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0eedb-1997">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="0eedb-1997">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0eedb-1998">Genel</span><span class="sxs-lookup"><span data-stu-id="0eedb-1998">General</span></span>
* <span data-ttu-id="0eedb-1999">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="0eedb-1999">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0eedb-2000">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eedb-2000">Az.Profile</span></span>
* <span data-ttu-id="0eedb-2001">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2001">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0eedb-2002">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2002">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0eedb-2003">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2003">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0eedb-2004">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2004">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0eedb-2005">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2005">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0eedb-2006">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2006">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0eedb-2007">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2007">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0eedb-2008">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-2008">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eedb-2009">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2009">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-2010">Az.Compute</span></span>
* <span data-ttu-id="0eedb-2011">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2011">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0eedb-2012">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-2012">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0eedb-2013">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2013">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-2014">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-2014">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-2015">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2015">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0eedb-2016">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2016">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0eedb-2017">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0eedb-2017">Az.Insights</span></span>
* <span data-ttu-id="0eedb-2018">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2018">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0eedb-2019">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="0eedb-2019">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0eedb-2020">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2020">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0eedb-2021">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-2021">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-2022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-2022">Az.Network</span></span>
* <span data-ttu-id="0eedb-2023">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="0eedb-2023">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0eedb-2024">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-2024">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0eedb-2025">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-2025">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0eedb-2026">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0eedb-2026">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0eedb-2027">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-2027">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0eedb-2028">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0eedb-2028">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0eedb-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0eedb-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0eedb-2030">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0eedb-2030">Az.PolicyInsights</span></span>
* <span data-ttu-id="0eedb-2031">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2031">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-2032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-2032">Az.Resources</span></span>
* <span data-ttu-id="0eedb-2033">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2033">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0eedb-2034">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="0eedb-2034">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0eedb-2035">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0eedb-2035">Az.ServiceBus</span></span>
* <span data-ttu-id="0eedb-2036">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2036">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0eedb-2037">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0eedb-2037">Az.ServiceFabric</span></span>
* <span data-ttu-id="0eedb-2038">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2038">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0eedb-2039">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2039">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0eedb-2040">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0eedb-2040">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0eedb-2041">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0eedb-2041">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0eedb-2042">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2042">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0eedb-2043">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="0eedb-2043">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0eedb-2044">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0eedb-2044">Az.Profile</span></span>
* <span data-ttu-id="0eedb-2045">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="0eedb-2045">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0eedb-2046">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2046">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-2047">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-2047">Az.Compute</span></span>
* <span data-ttu-id="0eedb-2048">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2048">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0eedb-2049">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2049">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0eedb-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0eedb-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="0eedb-2051">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="0eedb-2051">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0eedb-2052">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2052">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0eedb-2053">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0eedb-2054">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0eedb-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-2056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-2056">Az.Network</span></span>
* <span data-ttu-id="0eedb-2057">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2057">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0eedb-2058">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2058">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-2059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-2059">Az.Resources</span></span>
* <span data-ttu-id="0eedb-2060">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2060">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0eedb-2061">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2061">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0eedb-2062">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="0eedb-2062">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0eedb-2063">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="0eedb-2063">Azure.Storage</span></span>
* <span data-ttu-id="0eedb-2064">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="0eedb-2064">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0eedb-2065">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0eedb-2065">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0eedb-2066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0eedb-2066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0eedb-2067">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2067">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0eedb-2068">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0eedb-2068">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0eedb-2069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0eedb-2069">Az.CognitiveServices</span></span>
* <span data-ttu-id="0eedb-2070">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2070">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0eedb-2071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0eedb-2071">Az.Compute</span></span>
* <span data-ttu-id="0eedb-2072">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2072">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0eedb-2073">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2073">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0eedb-2074">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2074">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0eedb-2075">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0eedb-2075">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0eedb-2076">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2076">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0eedb-2077">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0eedb-2077">Az.Network</span></span>
* <span data-ttu-id="0eedb-2078">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2078">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0eedb-2079">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2079">new cmdlets added</span></span>
    - <span data-ttu-id="0eedb-2080">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eedb-2080">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eedb-2081">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eedb-2081">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eedb-2082">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eedb-2082">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eedb-2083">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0eedb-2083">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0eedb-2084">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-2084">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0eedb-2085">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0eedb-2085">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0eedb-2086">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2086">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0eedb-2087">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2087">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0eedb-2088">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2088">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0eedb-2089">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0eedb-2089">Az.RedisCache</span></span>
* <span data-ttu-id="0eedb-2090">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="0eedb-2090">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0eedb-2091">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2091">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0eedb-2092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0eedb-2092">Az.Resources</span></span>
* <span data-ttu-id="0eedb-2093">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2093">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0eedb-2094">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2094">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0eedb-2095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0eedb-2095">Az.Sql</span></span>
* <span data-ttu-id="0eedb-2096">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="0eedb-2096">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0eedb-2097">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0eedb-2097">Az.Websites</span></span>
* <span data-ttu-id="0eedb-2098">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-2098">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0eedb-2099">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="0eedb-2099">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0eedb-2100">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="0eedb-2100">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0eedb-2101">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="0eedb-2101">Initial Release</span></span>
