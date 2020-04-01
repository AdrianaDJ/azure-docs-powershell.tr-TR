---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 9e60e76206127922902804112e0b3f837cf03d76
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440512"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f9ef9-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="f9ef9-103">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="f9ef9-104">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="f9ef9-104">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-105">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-106">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-106">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-107">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-108">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-108">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="f9ef9-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f9ef9-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f9ef9-110">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-110">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f9ef9-111">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-111">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f9ef9-112">[#11354]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-112">[#11354]</span></span>
* <span data-ttu-id="f9ef9-113">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-113">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f9ef9-114">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-114">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f9ef9-115">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-115">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f9ef9-116">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-116">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f9ef9-117">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-117">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f9ef9-118">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-118">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f9ef9-119">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-119">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f9ef9-120">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-120">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f9ef9-121">[#11257]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-121">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-122">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-123">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-123">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f9ef9-124">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-124">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-126">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-126">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f9ef9-127">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-127">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9ef9-128">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9ef9-128">Az.HDInsight</span></span>
* <span data-ttu-id="f9ef9-129">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-129">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-130">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-130">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-131">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-131">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f9ef9-132">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9ef9-133">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-133">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f9ef9-134">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-134">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-135">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-136">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-136">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-137">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-137">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-138">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-138">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-139">Az.Network</span></span>
* <span data-ttu-id="f9ef9-140">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-140">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f9ef9-141">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-141">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f9ef9-142">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-142">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f9ef9-143">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-143">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f9ef9-144">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-144">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f9ef9-145">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-145">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9ef9-146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-146">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9ef9-147">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-147">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-149">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-149">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f9ef9-150">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-150">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f9ef9-151">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-151">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f9ef9-152">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-152">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f9ef9-153">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-153">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f9ef9-154">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-154">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-155">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-155">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-156">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-156">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f9ef9-157">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-157">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f9ef9-158">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-158">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f9ef9-159">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-159">Added example.</span></span>
* <span data-ttu-id="f9ef9-160">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-160">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f9ef9-161">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-161">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-162">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-163">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-163">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f9ef9-164">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-164">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f9ef9-165">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-165">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f9ef9-166">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f9ef9-166">Az.Support</span></span>
* <span data-ttu-id="f9ef9-167">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-167">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-168">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-169">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-169">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f9ef9-170">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-170">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f9ef9-171">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-171">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f9ef9-172">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-172">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f9ef9-173">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="f9ef9-173">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f9ef9-174">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="f9ef9-174">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-175">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-176">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-176">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f9ef9-177">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-177">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f9ef9-178">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-178">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-179">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-179">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-180">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-180">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f9ef9-181">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-181">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f9ef9-182">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-182">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f9ef9-183">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-183">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-184">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-184">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-185">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-185">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-186">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-186">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-187">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-187">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f9ef9-188">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-188">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9ef9-189">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-189">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9ef9-190">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-190">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9ef9-191">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-191">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9ef9-192">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-192">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f9ef9-193">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-193">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f9ef9-194">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-194">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9ef9-195">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-195">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f9ef9-196">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-196">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f9ef9-197">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-197">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f9ef9-198">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-198">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f9ef9-199">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-199">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f9ef9-200">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-200">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f9ef9-201">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-201">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f9ef9-202">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-202">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9ef9-203">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-203">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f9ef9-204">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-204">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f9ef9-205">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-205">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-206">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-207">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-207">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-208">Az.Network</span></span>
* <span data-ttu-id="f9ef9-209">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-209">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f9ef9-210">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-210">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f9ef9-211">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-211">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f9ef9-212">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-212">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-213">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-214">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-214">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f9ef9-215">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-215">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f9ef9-216">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-216">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f9ef9-217">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-217">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f9ef9-218">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-218">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f9ef9-219">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-219">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f9ef9-220">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-220">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f9ef9-221">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-221">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f9ef9-222">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ef9-222">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f9ef9-223">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ef9-223">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f9ef9-224">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ef9-224">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f9ef9-225">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-225">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f9ef9-226">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ef9-226">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f9ef9-227">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-227">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-228">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-229">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-229">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f9ef9-230">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-230">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f9ef9-231">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="f9ef9-231">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f9ef9-232">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-232">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f9ef9-233">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-233">Remove an LTR backup</span></span>
    - <span data-ttu-id="f9ef9-234">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-234">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f9ef9-235">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-235">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f9ef9-236">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-236">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f9ef9-237">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-237">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-238">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-238">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-239">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-239">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f9ef9-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f9ef9-241">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-241">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f9ef9-242">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-242">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f9ef9-243">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-243">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-244">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-245">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-245">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f9ef9-246">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-246">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f9ef9-247">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-247">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f9ef9-248">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-248">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f9ef9-249">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-249">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f9ef9-250">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="f9ef9-250">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9ef9-251">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="f9ef9-251">Highlights since the last major release</span></span>
* <span data-ttu-id="f9ef9-252">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-252">Updated client side telemetry.</span></span>
* <span data-ttu-id="f9ef9-253">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-253">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f9ef9-254">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-254">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-255">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-256">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-256">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-257">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-257">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-258">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-258">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9ef9-259">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-259">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9ef9-260">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-260">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f9ef9-261">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-261">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-262">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-263">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-263">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9ef9-264">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-264">Az.FrontDoor</span></span>
* <span data-ttu-id="f9ef9-265">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-265">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-266">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-266">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-267">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-267">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f9ef9-268">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-268">New Cmdlets are:</span></span>
    - <span data-ttu-id="f9ef9-269">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-269">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9ef9-270">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-270">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9ef9-271">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-271">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f9ef9-272">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-272">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-273">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-273">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-274">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-274">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-275">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-275">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-276">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-276">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f9ef9-277">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-277">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f9ef9-278">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-278">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-279">Az.Network</span></span>
* <span data-ttu-id="f9ef9-280">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-280">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f9ef9-281">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-281">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f9ef9-282">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-282">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f9ef9-283">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-283">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f9ef9-284">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-284">No new cmdlets are added.</span></span> <span data-ttu-id="f9ef9-285">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-285">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-287">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-287">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-288">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-289">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-289">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f9ef9-290">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9ef9-290">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f9ef9-291">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f9ef9-291">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f9ef9-292">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-292">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f9ef9-293">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-293">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f9ef9-294">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-294">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f9ef9-295">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-295">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f9ef9-296">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-296">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-297">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-297">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-298">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-298">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f9ef9-299">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-299">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f9ef9-300">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f9ef9-300">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f9ef9-301">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f9ef9-301">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f9ef9-302">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-302">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9ef9-303">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9ef9-303">Az.StorageSync</span></span>
* <span data-ttu-id="f9ef9-304">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-304">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f9ef9-305">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="f9ef9-305">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9ef9-306">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="f9ef9-306">Highlights since the last major release</span></span>
* <span data-ttu-id="f9ef9-307">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-307">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f9ef9-308">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-308">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-309">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-310">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-310">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f9ef9-311">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-311">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-312">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-312">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-313">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f9ef9-313">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f9ef9-314">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="f9ef9-314">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="f9ef9-315">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-315">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f9ef9-316">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-316">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-317">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-318">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-318">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f9ef9-319">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-319">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f9ef9-320">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-320">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f9ef9-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f9ef9-322">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-322">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-323">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-324">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-324">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f9ef9-325">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f9ef9-325">Az.DeploymentManager</span></span>
* <span data-ttu-id="f9ef9-326">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-326">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f9ef9-327">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-327">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9ef9-328">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9ef9-328">Az.HDInsight</span></span>
* <span data-ttu-id="f9ef9-329">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-329">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-330">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-330">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-331">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-331">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-332">Az.Network</span></span>
* <span data-ttu-id="f9ef9-333">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-333">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f9ef9-334">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="f9ef9-334">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f9ef9-335">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-335">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f9ef9-336">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-336">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f9ef9-337">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-337">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f9ef9-338">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-338">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f9ef9-339">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-339">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f9ef9-340">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-340">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f9ef9-341">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-341">New cmdlets added:</span></span>
        - <span data-ttu-id="f9ef9-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef9-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f9ef9-343">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-343">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f9ef9-344">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-344">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f9ef9-345">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-345">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9ef9-346">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-346">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9ef9-347">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-347">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f9ef9-348">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-348">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f9ef9-349">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-349">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f9ef9-350">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-350">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-352">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-352">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f9ef9-353">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-353">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-354">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-355">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-355">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f9ef9-356">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-356">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-357">Az.Sql</span></span>
<span data-ttu-id="f9ef9-358">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-358">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-359">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-360">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-360">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f9ef9-361">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-361">New-AzStorageAccount</span></span>
* <span data-ttu-id="f9ef9-362">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-362">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f9ef9-363">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-363">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-364">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-364">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-365">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="f9ef9-365">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f9ef9-366">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-366">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f9ef9-367">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="f9ef9-367">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-368">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-369">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-369">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9ef9-370">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9ef9-370">Az.Cdn</span></span>
* <span data-ttu-id="f9ef9-371">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-371">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-372">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-373">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-373">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f9ef9-374">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-374">Az.ContainerInstance</span></span>
* <span data-ttu-id="f9ef9-375">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-375">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f9ef9-376">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f9ef9-376">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f9ef9-377">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-377">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9ef9-378">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-378">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f9ef9-379">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-379">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9ef9-380">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-380">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f9ef9-381">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-381">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9ef9-382">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-382">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f9ef9-383">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-383">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f9ef9-384">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-384">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f9ef9-385">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-385">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f9ef9-386">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-386">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f9ef9-387">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-387">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f9ef9-388">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-388">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f9ef9-389">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-389">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f9ef9-390">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-390">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f9ef9-391">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-391">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f9ef9-392">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-392">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f9ef9-393">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-393">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f9ef9-394">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f9ef9-394">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-395">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-395">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-396">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-396">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f9ef9-397">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-397">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f9ef9-398">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-398">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f9ef9-399">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f9ef9-399">Az.DevTestLabs</span></span>
* <span data-ttu-id="f9ef9-400">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-400">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9ef9-401">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-401">Az.EventHub</span></span>
* <span data-ttu-id="f9ef9-402">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-402">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9ef9-403">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9ef9-403">Az.HDInsight</span></span>
* <span data-ttu-id="f9ef9-404">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-404">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f9ef9-405">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9ef9-405">Az.MachineLearning</span></span>
* <span data-ttu-id="f9ef9-406">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-406">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f9ef9-407">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9ef9-407">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9ef9-408">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="f9ef9-408">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f9ef9-409">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9ef9-409">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9ef9-410">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9ef9-410">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9ef9-411">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f9ef9-411">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f9ef9-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f9ef9-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f9ef9-413">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-413">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-414">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-414">Az.Network</span></span>
* <span data-ttu-id="f9ef9-415">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-415">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-417">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-417">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f9ef9-418">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-418">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f9ef9-419">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-419">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f9ef9-420">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-420">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-421">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-422">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-422">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-423">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-424">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-424">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f9ef9-425">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-425">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f9ef9-426">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f9ef9-426">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f9ef9-427">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-427">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-428">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-429">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-429">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f9ef9-430">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-430">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f9ef9-431">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-431">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f9ef9-432">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-432">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f9ef9-433">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-433">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f9ef9-434">Genel</span><span class="sxs-lookup"><span data-stu-id="f9ef9-434">General</span></span>
* <span data-ttu-id="f9ef9-435">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-435">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-436">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-436">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-437">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-437">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f9ef9-438">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-438">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9ef9-439">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9ef9-439">Az.Batch</span></span>
* <span data-ttu-id="f9ef9-440">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-440">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-441">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-442">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-442">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9ef9-443">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-443">Az.FrontDoor</span></span>
* <span data-ttu-id="f9ef9-444">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-444">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f9ef9-445">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-445">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f9ef9-446">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f9ef9-446">Az.HealthcareApis</span></span>
* <span data-ttu-id="f9ef9-447">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-447">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-448">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-449">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-449">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f9ef9-450">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-450">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f9ef9-451">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-451">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-452">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-453">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-453">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f9ef9-454">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="f9ef9-454">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f9ef9-455">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="f9ef9-455">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-456">Az.Network</span></span>
* <span data-ttu-id="f9ef9-457">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-457">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-458">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-459">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-459">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f9ef9-460">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-460">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-461">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-461">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-462">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-462">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-463">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-464">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-464">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f9ef9-465">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f9ef9-465">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f9ef9-466">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f9ef9-466">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f9ef9-467">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-467">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f9ef9-468">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f9ef9-468">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f9ef9-469">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-469">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f9ef9-470">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-470">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f9ef9-471">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9ef9-471">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f9ef9-472">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9ef9-472">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f9ef9-473">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-473">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f9ef9-474">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f9ef9-474">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f9ef9-475">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-475">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f9ef9-476">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f9ef9-476">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f9ef9-477">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-477">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9ef9-478">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="f9ef9-478">Highlights since the last major release</span></span>
* <span data-ttu-id="f9ef9-479">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-479">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f9ef9-480">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-480">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-481">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-482">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-482">VM Reapply feature</span></span>
    - <span data-ttu-id="f9ef9-483">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-483">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f9ef9-484">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-484">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f9ef9-485">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f9ef9-485">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f9ef9-486">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-486">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f9ef9-487">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-487">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f9ef9-488">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-488">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f9ef9-489">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-489">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f9ef9-490">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-490">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f9ef9-491">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-491">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f9ef9-492">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-492">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f9ef9-493">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f9ef9-493">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f9ef9-494">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-494">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f9ef9-495">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="f9ef9-495">Get the Order</span></span>
* <span data-ttu-id="f9ef9-496">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-496">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f9ef9-497">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-497">Create new Order</span></span>
* <span data-ttu-id="f9ef9-498">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-498">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f9ef9-499">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-499">Remove the Order</span></span>
* <span data-ttu-id="f9ef9-500">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-500">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f9ef9-501">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-501">Now creates Local Share</span></span>
* <span data-ttu-id="f9ef9-502">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-502">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f9ef9-503">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-503">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f9ef9-504">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-504">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f9ef9-505">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="f9ef9-505">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f9ef9-506">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-506">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f9ef9-507">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-507">Gets the information about Triggers</span></span>
* <span data-ttu-id="f9ef9-508">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-508">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f9ef9-509">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-509">Create new Triggers</span></span>
* <span data-ttu-id="f9ef9-510">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-510">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f9ef9-511">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-511">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-512">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-512">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-513">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-513">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f9ef9-514">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-514">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-515">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-515">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-516">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-516">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9ef9-517">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-517">Az.EventHub</span></span>
* <span data-ttu-id="f9ef9-518">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-518">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9ef9-519">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-519">Az.FrontDoor</span></span>
* <span data-ttu-id="f9ef9-520">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-520">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f9ef9-521">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-521">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f9ef9-522">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-522">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f9ef9-523">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f9ef9-523">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-524">Az.Network</span></span>
* <span data-ttu-id="f9ef9-525">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-525">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f9ef9-526">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f9ef9-526">Az.PrivateDns</span></span>
* <span data-ttu-id="f9ef9-527">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-527">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-529">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-529">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f9ef9-530">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-530">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f9ef9-531">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-531">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9ef9-532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9ef9-532">Az.RedisCache</span></span>
* <span data-ttu-id="f9ef9-533">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-533">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f9ef9-534">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-534">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f9ef9-535">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-535">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-536">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-536">Az.Resources</span></span>
- <span data-ttu-id="f9ef9-537">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-537">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f9ef9-538">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-538">Updated create policy definition help example</span></span>
- <span data-ttu-id="f9ef9-539">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-539">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f9ef9-540">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-540">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f9ef9-541">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-541">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-542">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-542">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-543">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-543">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f9ef9-544">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-544">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f9ef9-545">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-545">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f9ef9-546">Genel</span><span class="sxs-lookup"><span data-stu-id="f9ef9-546">General</span></span>
* <span data-ttu-id="f9ef9-547">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-547">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-548">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-549">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-549">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f9ef9-550">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-550">Az.Advisor</span></span>
* <span data-ttu-id="f9ef9-551">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-551">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9ef9-552">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9ef9-552">Az.Batch</span></span>
* <span data-ttu-id="f9ef9-553">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-553">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f9ef9-554">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-554">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f9ef9-555">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-555">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f9ef9-556">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-556">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f9ef9-557">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-557">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f9ef9-558">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-558">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f9ef9-559">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-559">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f9ef9-560">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-560">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f9ef9-561">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-561">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f9ef9-562">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-562">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f9ef9-563">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-563">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f9ef9-564">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-564">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f9ef9-565">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-565">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f9ef9-566">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-566">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f9ef9-567">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-567">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f9ef9-568">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-568">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f9ef9-569">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-569">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f9ef9-570">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-570">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f9ef9-571">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-571">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f9ef9-572">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-572">This operation is no longer supported.</span></span>
* <span data-ttu-id="f9ef9-573">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-573">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f9ef9-574">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-574">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f9ef9-575">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-575">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f9ef9-576">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-576">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f9ef9-577">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-577">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f9ef9-578">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-578">New non-verified images are also now returned.</span></span> <span data-ttu-id="f9ef9-579">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-579">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f9ef9-580">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-580">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f9ef9-581">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-581">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f9ef9-582">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-582">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f9ef9-583">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-583">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f9ef9-584">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-584">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f9ef9-585">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-585">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f9ef9-586">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-586">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f9ef9-587">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-587">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f9ef9-588">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-588">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9ef9-589">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9ef9-589">Az.Cdn</span></span>
* <span data-ttu-id="f9ef9-590">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-590">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f9ef9-591">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-591">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-592">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-592">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-593">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-593">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f9ef9-594">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-594">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f9ef9-595">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f9ef9-595">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f9ef9-596">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-596">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f9ef9-597">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-597">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f9ef9-598">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-598">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f9ef9-599">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-599">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f9ef9-600">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-600">Breaking changes</span></span>
    - <span data-ttu-id="f9ef9-601">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-601">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f9ef9-602">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-602">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-603">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-603">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-604">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-604">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-605">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-605">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-606">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-606">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f9ef9-607">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-607">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f9ef9-608">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-608">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f9ef9-609">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-609">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f9ef9-610">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-610">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f9ef9-611">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-611">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9ef9-612">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-612">Az.FrontDoor</span></span>
* <span data-ttu-id="f9ef9-613">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-613">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9ef9-614">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9ef9-614">Az.HDInsight</span></span>
* <span data-ttu-id="f9ef9-615">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-615">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f9ef9-616">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-616">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f9ef9-617">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-617">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f9ef9-618">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-618">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f9ef9-619">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f9ef9-619">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f9ef9-620">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f9ef9-620">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f9ef9-621">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f9ef9-621">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f9ef9-622">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9ef9-622">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f9ef9-623">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9ef9-623">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f9ef9-624">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-624">Added three cmdlets:</span></span>
    - <span data-ttu-id="f9ef9-625">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-625">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f9ef9-626">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-626">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f9ef9-627">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-627">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f9ef9-628">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-628">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f9ef9-629">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-629">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f9ef9-630">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-630">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f9ef9-631">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-631">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f9ef9-632">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-632">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f9ef9-633">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-633">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f9ef9-634">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-634">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f9ef9-635">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-635">Added some scenario test cases.</span></span>
* <span data-ttu-id="f9ef9-636">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-636">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-637">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-637">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-638">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-638">Breaking changes:</span></span>
    - <span data-ttu-id="f9ef9-639">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-639">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9ef9-640">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-640">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f9ef9-641">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-641">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9ef9-642">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-642">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f9ef9-643">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-643">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f9ef9-644">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-644">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f9ef9-645">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-645">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f9ef9-646">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-646">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f9ef9-647">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-647">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9ef9-648">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-648">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f9ef9-649">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-649">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f9ef9-650">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-650">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-651">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-651">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-652">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-652">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f9ef9-653">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-653">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f9ef9-654">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-654">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f9ef9-655">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-655">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f9ef9-656">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-656">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f9ef9-657">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-657">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f9ef9-658">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-658">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f9ef9-659">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-659">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f9ef9-660">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-660">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-661">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-662">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-662">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-663">Az.Network</span></span>
* <span data-ttu-id="f9ef9-664">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-664">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f9ef9-665">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-665">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9ef9-666">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-666">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-667">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-667">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-668">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-668">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-669">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-669">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-670">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-670">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f9ef9-671">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-671">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f9ef9-672">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-672">New cmdlet:</span></span>
        - <span data-ttu-id="f9ef9-673">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f9ef9-673">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f9ef9-674">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-674">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f9ef9-675">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-675">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f9ef9-676">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-676">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f9ef9-677">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-677">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f9ef9-678">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-678">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f9ef9-679">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-679">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f9ef9-680">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-680">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f9ef9-681">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-681">New cmdlets added:</span></span>
        - <span data-ttu-id="f9ef9-682">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-682">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f9ef9-683">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-683">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f9ef9-684">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-684">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f9ef9-685">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-685">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f9ef9-686">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-686">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f9ef9-687">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-687">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f9ef9-688">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-688">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9ef9-689">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-689">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f9ef9-690">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-690">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f9ef9-691">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-691">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f9ef9-692">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-692">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f9ef9-693">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-693">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f9ef9-694">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-694">New cmdlets added:</span></span>
        - <span data-ttu-id="f9ef9-695">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-695">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f9ef9-696">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-696">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9ef9-697">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-697">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9ef9-698">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-698">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9ef9-699">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-699">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9ef9-700">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-700">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f9ef9-701">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-701">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f9ef9-702">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-702">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f9ef9-703">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-703">New cmdlets added:</span></span>
        - <span data-ttu-id="f9ef9-704">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f9ef9-704">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f9ef9-705">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f9ef9-705">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f9ef9-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f9ef9-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f9ef9-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f9ef9-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f9ef9-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f9ef9-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f9ef9-710">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9ef9-711">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-711">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f9ef9-712">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-712">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f9ef9-713">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-713">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f9ef9-714">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-714">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f9ef9-715">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-715">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f9ef9-716">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-716">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f9ef9-717">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-717">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f9ef9-718">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-718">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f9ef9-719">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-719">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f9ef9-720">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-720">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f9ef9-721">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-721">New cmdlets added:</span></span>
        - <span data-ttu-id="f9ef9-722">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9ef9-722">New-AzIpGroup</span></span>
        - <span data-ttu-id="f9ef9-723">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9ef9-723">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f9ef9-724">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9ef9-724">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f9ef9-725">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f9ef9-725">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-726">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-726">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-727">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-727">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-728">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-729">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-729">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f9ef9-730">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-730">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f9ef9-731">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-731">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f9ef9-732">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-732">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f9ef9-733">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-733">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f9ef9-734">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-734">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f9ef9-735">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-735">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f9ef9-736">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-736">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f9ef9-737">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-737">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-738">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-738">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-739">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-739">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f9ef9-740">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-740">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f9ef9-741">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-741">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f9ef9-742">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="f9ef9-742">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f9ef9-743">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9ef9-743">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f9ef9-744">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9ef9-744">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f9ef9-745">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-745">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f9ef9-746">Genel</span><span class="sxs-lookup"><span data-stu-id="f9ef9-746">General</span></span>
* <span data-ttu-id="f9ef9-747">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-747">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-748">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-748">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-749">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-749">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-750">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-751">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-751">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f9ef9-752">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-752">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-753">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-753">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-754">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-754">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9ef9-755">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9ef9-755">Az.Batch</span></span>
* <span data-ttu-id="f9ef9-756">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-756">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-757">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-758">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-758">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f9ef9-759">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-759">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f9ef9-760">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-760">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f9ef9-761">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-761">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-762">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-763">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-763">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f9ef9-764">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-764">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f9ef9-765">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-765">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-766">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-767">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-767">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f9ef9-768">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f9ef9-768">Az.HealthcareApis</span></span>
* <span data-ttu-id="f9ef9-769">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-769">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f9ef9-770">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-770">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f9ef9-771">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-771">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f9ef9-772">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-772">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-773">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-773">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-774">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f9ef9-774">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f9ef9-775">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-775">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-776">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-776">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-777">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-777">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f9ef9-778">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-778">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f9ef9-779">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-779">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f9ef9-780">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-780">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-781">Az.Network</span></span>
* <span data-ttu-id="f9ef9-782">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-782">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f9ef9-783">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-783">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f9ef9-784">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-784">New cmdlets added:</span></span>
        - <span data-ttu-id="f9ef9-785">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-785">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f9ef9-786">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-786">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9ef9-787">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-787">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f9ef9-788">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-788">Updated cmdlets:</span></span>
        - <span data-ttu-id="f9ef9-789">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-789">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9ef9-790">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-790">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9ef9-791">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-791">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f9ef9-792">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-792">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f9ef9-793">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="f9ef9-793">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f9ef9-794">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-794">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f9ef9-795">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-795">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9ef9-796">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9ef9-796">Az.RedisCache</span></span>
* <span data-ttu-id="f9ef9-797">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-797">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-798">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-799">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-799">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-800">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-800">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-801">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-801">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f9ef9-802">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-802">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f9ef9-803">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9ef9-803">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f9ef9-804">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-804">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f9ef9-805">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-805">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9ef9-806">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9ef9-806">Az.StorageSync</span></span>
* <span data-ttu-id="f9ef9-807">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-807">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-808">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-808">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-809">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-809">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f9ef9-810">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-810">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-811">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-812">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-812">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f9ef9-813">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-813">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f9ef9-814">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-814">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-815">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-815">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-816">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-816">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f9ef9-817">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-817">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f9ef9-818">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-818">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-819">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-820">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-820">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f9ef9-821">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-821">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f9ef9-822">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-822">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f9ef9-823">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-823">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f9ef9-824">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-824">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f9ef9-825">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-825">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f9ef9-826">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-826">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f9ef9-827">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-827">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f9ef9-828">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-828">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-829">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-829">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-830">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f9ef9-830">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f9ef9-831">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-831">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9ef9-832">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9ef9-832">Az.HDInsight</span></span>
* <span data-ttu-id="f9ef9-833">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-833">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-834">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-835">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-835">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f9ef9-836">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-836">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f9ef9-837">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-837">New cmdlets are:</span></span>
    - <span data-ttu-id="f9ef9-838">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9ef9-838">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f9ef9-839">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9ef9-839">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f9ef9-840">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9ef9-840">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f9ef9-841">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f9ef9-841">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-842">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-843">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="f9ef9-843">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f9ef9-844">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-844">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f9ef9-845">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-845">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f9ef9-846">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-846">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f9ef9-847">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-847">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f9ef9-848">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-848">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f9ef9-849">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-849">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f9ef9-850">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-850">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f9ef9-851">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-851">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f9ef9-852">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-852">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f9ef9-853">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-853">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f9ef9-854">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-854">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f9ef9-855">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-855">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f9ef9-856">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-856">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f9ef9-857">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="f9ef9-857">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f9ef9-858">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-858">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f9ef9-859">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="f9ef9-859">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f9ef9-860">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-860">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f9ef9-861">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-861">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f9ef9-862">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-862">Overall improved help files</span></span>
* <span data-ttu-id="f9ef9-863">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-863">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-864">Az.Network</span></span>
* <span data-ttu-id="f9ef9-865">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-865">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f9ef9-866">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-866">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f9ef9-867">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-867">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f9ef9-868">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-868">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f9ef9-869">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-869">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f9ef9-870">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-870">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f9ef9-871">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-871">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f9ef9-872">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-872">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f9ef9-873">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-873">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f9ef9-874">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-874">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f9ef9-875">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-875">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f9ef9-876">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-876">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f9ef9-877">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-877">New cmdlets</span></span>
        - <span data-ttu-id="f9ef9-878">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f9ef9-878">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f9ef9-879">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-879">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f9ef9-880">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-880">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9ef9-881">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f9ef9-881">New-VpnSite</span></span>
        - <span data-ttu-id="f9ef9-882">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f9ef9-882">Update-VpnSite</span></span>
        - <span data-ttu-id="f9ef9-883">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-883">New-VpnConnection</span></span>
        - <span data-ttu-id="f9ef9-884">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-884">Update-VpnConnection</span></span>
* <span data-ttu-id="f9ef9-885">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-885">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-887">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-887">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f9ef9-888">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-888">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-889">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-890">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-890">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-891">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-891">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-892">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-892">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f9ef9-893">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-893">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f9ef9-894">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9ef9-894">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9ef9-895">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f9ef9-895">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f9ef9-896">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f9ef9-896">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f9ef9-897">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-897">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f9ef9-898">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9ef9-898">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9ef9-899">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9ef9-899">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9ef9-900">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f9ef9-900">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f9ef9-901">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f9ef9-901">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f9ef9-902">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-902">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f9ef9-903">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f9ef9-903">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f9ef9-904">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f9ef9-904">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f9ef9-905">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f9ef9-905">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f9ef9-906">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f9ef9-906">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f9ef9-907">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-907">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f9ef9-908">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f9ef9-908">Az.SignalR</span></span>
* <span data-ttu-id="f9ef9-909">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-909">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-910">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-910">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-911">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-911">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f9ef9-912">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-912">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f9ef9-913">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-913">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f9ef9-914">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-914">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f9ef9-915">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-915">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-916">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-917">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-917">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f9ef9-918">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-918">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f9ef9-919">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-919">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f9ef9-920">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-920">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f9ef9-921">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-921">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f9ef9-922">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-922">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f9ef9-923">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-923">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f9ef9-924">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9ef9-924">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f9ef9-925">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9ef9-925">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f9ef9-926">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9ef9-926">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f9ef9-927">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f9ef9-927">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-928">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-928">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-929">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-929">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f9ef9-930">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-930">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f9ef9-931">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-931">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f9ef9-932">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-932">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f9ef9-933">Genel</span><span class="sxs-lookup"><span data-stu-id="f9ef9-933">General</span></span>
* <span data-ttu-id="f9ef9-934">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-934">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-935">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-935">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-936">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-936">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f9ef9-937">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f9ef9-937">Az.Aks</span></span>
* <span data-ttu-id="f9ef9-938">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-938">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f9ef9-939">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f9ef9-939">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-940">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-940">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-941">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-941">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f9ef9-942">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-942">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f9ef9-943">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-943">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f9ef9-944">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f9ef9-944">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f9ef9-945">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-945">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9ef9-946">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9ef9-946">Az.Batch</span></span>
* <span data-ttu-id="f9ef9-947">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-947">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9ef9-948">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9ef9-948">Az.Cdn</span></span>
* <span data-ttu-id="f9ef9-949">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-949">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-950">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-950">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-951">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-951">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f9ef9-952">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-952">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f9ef9-953">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-953">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f9ef9-954">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-954">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f9ef9-955">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f9ef9-955">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f9ef9-956">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-956">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f9ef9-957">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-957">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f9ef9-958">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-958">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-959">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-960">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-960">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f9ef9-961">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-961">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f9ef9-962">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-962">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f9ef9-963">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-963">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-964">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-964">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-965">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-965">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9ef9-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-966">Az.EventHub</span></span>
* <span data-ttu-id="f9ef9-967">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="f9ef9-967">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f9ef9-968">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="f9ef9-968">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f9ef9-969">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-969">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f9ef9-970">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="f9ef9-970">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f9ef9-971">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f9ef9-971">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f9ef9-972">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-972">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-973">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-974">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-974">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-975">Az.Network</span></span>
* <span data-ttu-id="f9ef9-976">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-976">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f9ef9-977">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-977">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f9ef9-978">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-978">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f9ef9-979">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-979">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f9ef9-980">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-980">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f9ef9-981">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-981">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f9ef9-982">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-982">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9ef9-983">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-983">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9ef9-984">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-984">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f9ef9-985">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-985">Added example</span></span>
    - <span data-ttu-id="f9ef9-986">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-986">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f9ef9-987">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-987">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f9ef9-988">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-988">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-990">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-990">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-991">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-991">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-992">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-992">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f9ef9-993">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-993">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f9ef9-994">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-994">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f9ef9-995">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-995">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9ef9-996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9ef9-996">Az.ServiceBus</span></span>
* <span data-ttu-id="f9ef9-997">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="f9ef9-997">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f9ef9-998">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="f9ef9-998">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f9ef9-999">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-999">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-1000">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1000">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-1001">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1001">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f9ef9-1002">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1002">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f9ef9-1003">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1003">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f9ef9-1004">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1004">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f9ef9-1005">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1005">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f9ef9-1006">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1006">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1007">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1007">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1008">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1008">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1009">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1009">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1010">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1010">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f9ef9-1011">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1011">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f9ef9-1012">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1012">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f9ef9-1013">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1013">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f9ef9-1014">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1014">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f9ef9-1015">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1015">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1016">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1016">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1017">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1017">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f9ef9-1018">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1018">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1019">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1019">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1020">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1020">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f9ef9-1021">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1021">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f9ef9-1022">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1022">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1023">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1024">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1024">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9ef9-1025">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1025">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9ef9-1026">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1026">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1027">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1028">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1028">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f9ef9-1029">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1029">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f9ef9-1030">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1030">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f9ef9-1031">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1031">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-1032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1032">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-1033">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1033">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f9ef9-1034">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1034">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9ef9-1035">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1035">Az.EventHub</span></span>
* <span data-ttu-id="f9ef9-1036">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1036">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f9ef9-1037">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1037">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-1038">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1038">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-1039">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1039">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9ef9-1040">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1040">Az.LogicApp</span></span>
* <span data-ttu-id="f9ef9-1041">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1041">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f9ef9-1042">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1042">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f9ef9-1043">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1043">Az.ManagedServices</span></span>
* <span data-ttu-id="f9ef9-1044">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1044">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1045">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1045">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1046">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1046">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f9ef9-1047">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1047">New cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1048">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1048">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9ef9-1049">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1049">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9ef9-1050">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1050">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-1051">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1051">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-1052">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1052">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-1053">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1053">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f9ef9-1054">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1054">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f9ef9-1055">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1055">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f9ef9-1056">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1056">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f9ef9-1057">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1057">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f9ef9-1058">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1058">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f9ef9-1059">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1059">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f9ef9-1060">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1060">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f9ef9-1061">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1061">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f9ef9-1062">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1062">Updated cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1063">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1063">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9ef9-1064">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1064">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f9ef9-1065">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1065">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f9ef9-1066">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1066">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f9ef9-1067">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1067">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f9ef9-1068">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1068">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9ef9-1069">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1069">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f9ef9-1070">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1070">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f9ef9-1071">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1071">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f9ef9-1072">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1072">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f9ef9-1073">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1073">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f9ef9-1074">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1074">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9ef9-1075">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1075">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9ef9-1076">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1076">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f9ef9-1077">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1077">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1078">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1078">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1079">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1079">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f9ef9-1080">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1080">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f9ef9-1081">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1081">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f9ef9-1082">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1082">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f9ef9-1083">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1083">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f9ef9-1084">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1084">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f9ef9-1085">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1085">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f9ef9-1086">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1086">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f9ef9-1087">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1087">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f9ef9-1088">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1088">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1089">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1089">Az.Resources</span></span>
- <span data-ttu-id="f9ef9-1090">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1090">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f9ef9-1091">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1091">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9ef9-1092">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1092">Az.ServiceBus</span></span>
* <span data-ttu-id="f9ef9-1093">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1093">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f9ef9-1094">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1094">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1095">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1096">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1096">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f9ef9-1097">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1097">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f9ef9-1098">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1098">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1099">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1100">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1100">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9ef9-1101">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1101">Az.StorageSync</span></span>
* <span data-ttu-id="f9ef9-1102">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1102">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f9ef9-1103">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1103">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1104">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1104">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1105">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1105">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f9ef9-1106">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1106">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f9ef9-1107">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1107">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f9ef9-1108">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1108">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1109">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1110">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1110">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f9ef9-1111">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1111">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f9ef9-1112">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1112">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f9ef9-1113">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1113">Az.Advisor</span></span>
* <span data-ttu-id="f9ef9-1114">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1114">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f9ef9-1115">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1115">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-1116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1116">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-1117">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f9ef9-1118">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1118">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f9ef9-1119">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1119">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f9ef9-1120">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1120">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f9ef9-1121">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f9ef9-1122">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1122">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f9ef9-1123">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1123">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1124">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1124">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1125">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1125">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1126">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1126">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1127">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1127">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1128">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-1129">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1129">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9ef9-1130">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1130">Az.EventGrid</span></span>
* <span data-ttu-id="f9ef9-1131">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1131">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-1132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1132">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-1133">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1133">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1134">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1135">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1135">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f9ef9-1136">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1136">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9ef9-1137">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1137">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9ef9-1138">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1138">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f9ef9-1139">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1139">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9ef9-1140">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1140">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9ef9-1141">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1141">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1143">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1143">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1144">Az.Resources</span></span>
    - <span data-ttu-id="f9ef9-1145">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1145">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f9ef9-1146">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1146">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f9ef9-1147">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1147">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f9ef9-1148">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1148">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9ef9-1149">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1149">Az.ServiceBus</span></span>
* <span data-ttu-id="f9ef9-1150">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1150">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1151">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1152">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1152">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f9ef9-1153">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1153">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f9ef9-1154">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1154">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f9ef9-1155">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1155">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f9ef9-1156">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1156">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f9ef9-1157">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1157">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f9ef9-1158">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1158">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f9ef9-1159">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1159">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f9ef9-1160">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1160">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1161">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1162">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1162">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f9ef9-1163">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1163">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f9ef9-1164">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1164">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f9ef9-1165">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1165">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f9ef9-1166">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1166">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f9ef9-1167">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1167">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f9ef9-1168">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1168">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f9ef9-1169">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1169">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f9ef9-1170">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1170">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f9ef9-1171">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1171">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f9ef9-1172">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1172">Az.StorageSync</span></span>
* <span data-ttu-id="f9ef9-1173">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1173">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f9ef9-1174">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1174">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1175">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1176">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1176">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f9ef9-1177">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1177">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f9ef9-1178">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1178">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f9ef9-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f9ef9-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1181">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1181">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1182">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1182">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f9ef9-1183">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1183">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f9ef9-1184">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1184">Az.Dns</span></span>
* <span data-ttu-id="f9ef9-1185">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1185">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9ef9-1186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1186">Az.EventGrid</span></span>
* <span data-ttu-id="f9ef9-1187">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1187">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f9ef9-1188">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1188">New cmdlets:</span></span>
    - <span data-ttu-id="f9ef9-1189">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1189">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f9ef9-1190">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1190">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f9ef9-1191">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1191">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f9ef9-1192">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1192">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f9ef9-1193">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1193">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f9ef9-1194">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1194">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f9ef9-1195">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1195">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f9ef9-1196">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1196">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f9ef9-1197">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1197">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f9ef9-1198">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1198">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f9ef9-1199">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1199">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f9ef9-1200">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1200">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f9ef9-1201">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1201">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f9ef9-1202">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1202">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f9ef9-1203">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1203">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f9ef9-1204">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1204">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f9ef9-1205">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1205">Updated cmdlets:</span></span>
    - <span data-ttu-id="f9ef9-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f9ef9-1207">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1207">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f9ef9-1208">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1208">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f9ef9-1209">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1209">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f9ef9-1210">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1210">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f9ef9-1211">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1211">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f9ef9-1212">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1212">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f9ef9-1213">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1213">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f9ef9-1214">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1214">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f9ef9-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f9ef9-1216">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1216">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f9ef9-1217">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1217">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f9ef9-1218">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1218">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f9ef9-1219">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1219">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9ef9-1220">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1220">Az.FrontDoor</span></span>
* <span data-ttu-id="f9ef9-1221">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1221">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f9ef9-1222">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1222">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f9ef9-1223">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1223">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f9ef9-1224">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1224">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1225">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1226">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1226">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f9ef9-1227">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1227">New cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f9ef9-1229">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1229">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f9ef9-1230">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1230">New cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1231">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1231">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f9ef9-1232">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1232">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f9ef9-1233">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1233">New cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1234">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1234">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9ef9-1235">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1235">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9ef9-1236">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1236">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f9ef9-1237">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1237">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f9ef9-1238">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1238">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f9ef9-1239">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1239">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f9ef9-1240">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1240">New cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1241">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1241">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9ef9-1242">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1242">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9ef9-1243">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1243">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f9ef9-1244">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1244">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f9ef9-1245">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1245">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f9ef9-1246">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1246">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f9ef9-1247">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1247">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f9ef9-1248">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1248">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f9ef9-1249">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1249">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f9ef9-1250">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1250">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f9ef9-1251">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1251">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f9ef9-1252">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1252">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f9ef9-1253">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1253">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f9ef9-1254">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1254">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f9ef9-1255">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1255">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f9ef9-1256">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1256">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f9ef9-1257">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1257">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f9ef9-1258">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1258">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f9ef9-1259">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1259">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f9ef9-1260">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1260">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f9ef9-1261">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1261">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f9ef9-1262">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1262">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f9ef9-1263">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1263">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f9ef9-1264">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1264">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f9ef9-1265">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1265">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f9ef9-1266">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1266">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f9ef9-1267">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1267">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9ef9-1268">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1268">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9ef9-1269">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1269">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1270">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1271">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1271">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f9ef9-1272">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1272">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f9ef9-1273">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1273">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f9ef9-1274">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1274">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-1276">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1276">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1277">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1278">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1278">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f9ef9-1279">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1279">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f9ef9-1280">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1280">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f9ef9-1281">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1281">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f9ef9-1282">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1282">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f9ef9-1283">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1283">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f9ef9-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f9ef9-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1286">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1287">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1287">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f9ef9-1288">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1288">New-AzStorageAccount</span></span>
* <span data-ttu-id="f9ef9-1289">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1289">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f9ef9-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1291">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1291">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1292">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1292">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f9ef9-1293">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1293">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f9ef9-1294">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1294">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f9ef9-1295">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1295">Az.Cdn</span></span>
* <span data-ttu-id="f9ef9-1296">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1296">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1297">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1297">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1298">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1298">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f9ef9-1299">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1299">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9ef9-1300">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1300">Az.EventHub</span></span>
* <span data-ttu-id="f9ef9-1301">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1301">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f9ef9-1302">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1302">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1303">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1304">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1304">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f9ef9-1305">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1305">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9ef9-1306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1306">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9ef9-1307">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1307">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1309">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1309">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9ef9-1310">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1310">Az.ServiceBus</span></span>
* <span data-ttu-id="f9ef9-1311">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1311">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-1312">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1312">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-1313">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1313">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f9ef9-1314">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1314">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1315">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1316">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1316">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f9ef9-1317">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1317">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f9ef9-1318">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1318">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f9ef9-1319">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1319">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1320">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1320">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1321">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1321">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f9ef9-1322">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1322">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-1323">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1323">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-1324">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1324">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f9ef9-1325">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1325">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f9ef9-1326">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1326">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f9ef9-1327">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1327">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f9ef9-1328">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1328">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f9ef9-1329">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1329">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f9ef9-1330">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1330">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f9ef9-1331">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1331">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f9ef9-1332">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1332">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f9ef9-1333">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1333">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f9ef9-1334">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1334">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f9ef9-1335">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1335">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f9ef9-1336">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1336">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f9ef9-1337">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1337">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f9ef9-1338">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1338">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f9ef9-1339">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1339">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f9ef9-1340">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1340">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f9ef9-1341">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1341">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f9ef9-1342">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1342">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f9ef9-1343">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1343">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f9ef9-1344">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1344">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f9ef9-1345">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1345">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f9ef9-1346">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1346">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f9ef9-1347">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1347">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f9ef9-1348">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1348">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f9ef9-1349">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1349">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f9ef9-1350">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1350">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f9ef9-1351">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1351">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f9ef9-1352">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1352">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f9ef9-1353">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1353">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f9ef9-1354">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1354">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f9ef9-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f9ef9-1356">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1356">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f9ef9-1357">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1357">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f9ef9-1358">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1358">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f9ef9-1359">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1359">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f9ef9-1360">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1360">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f9ef9-1361">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1361">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f9ef9-1362">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1362">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f9ef9-1363">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1363">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f9ef9-1364">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1364">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f9ef9-1365">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1365">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f9ef9-1366">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1366">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f9ef9-1367">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1367">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f9ef9-1368">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1368">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f9ef9-1369">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1369">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f9ef9-1370">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1370">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f9ef9-1371">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1371">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f9ef9-1372">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1372">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f9ef9-1373">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1373">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f9ef9-1374">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1374">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f9ef9-1375">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1375">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f9ef9-1376">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1376">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f9ef9-1377">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1377">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f9ef9-1378">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1378">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f9ef9-1379">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1379">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f9ef9-1380">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1380">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f9ef9-1381">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1381">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f9ef9-1382">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1382">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f9ef9-1383">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1383">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f9ef9-1384">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1384">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f9ef9-1385">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1385">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f9ef9-1386">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1386">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f9ef9-1387">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1387">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f9ef9-1388">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1388">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f9ef9-1389">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1389">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f9ef9-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f9ef9-1391">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1391">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f9ef9-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f9ef9-1393">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1393">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f9ef9-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f9ef9-1395">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1395">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f9ef9-1396">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1396">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f9ef9-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f9ef9-1398">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1398">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f9ef9-1399">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1399">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f9ef9-1400">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1400">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1401">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1401">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1402">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1402">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f9ef9-1403">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1403">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f9ef9-1404">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1404">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f9ef9-1405">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1405">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f9ef9-1406">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1406">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f9ef9-1407">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1407">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f9ef9-1408">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1408">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1409">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1410">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1410">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f9ef9-1411">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1411">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-1413">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1413">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-1414">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1414">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-1415">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1415">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1416">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1417">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1417">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f9ef9-1418">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1418">Updated cmdlet:</span></span>
        - <span data-ttu-id="f9ef9-1419">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1419">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f9ef9-1420">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1420">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1421">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1422">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1422">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1423">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1424">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1424">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f9ef9-1425">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1425">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1426">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1427">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1427">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9ef9-1428">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1428">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9ef9-1429">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1429">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f9ef9-1430">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1430">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1431">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1432">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1432">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f9ef9-1433">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1433">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f9ef9-1434">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1434">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f9ef9-1435">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1435">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f9ef9-1436">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1436">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f9ef9-1437">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1437">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f9ef9-1438">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1438">Breaking changes</span></span>
    - <span data-ttu-id="f9ef9-1439">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1439">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f9ef9-1440">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1440">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f9ef9-1441">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1441">Az.DeploymentManager</span></span>
* <span data-ttu-id="f9ef9-1442">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1442">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f9ef9-1443">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1443">Az.Dns</span></span>
* <span data-ttu-id="f9ef9-1444">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1444">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f9ef9-1445">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1445">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f9ef9-1446">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1446">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f9ef9-1447">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1447">Az.FrontDoor</span></span>
* <span data-ttu-id="f9ef9-1448">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1448">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f9ef9-1449">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1449">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f9ef9-1450">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1450">Az.HDInsight</span></span>
* <span data-ttu-id="f9ef9-1451">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1451">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f9ef9-1452">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1452">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f9ef9-1453">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1453">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f9ef9-1454">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1454">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f9ef9-1455">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1455">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f9ef9-1456">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1456">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f9ef9-1457">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1457">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-1458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1458">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-1459">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1459">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f9ef9-1460">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1460">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f9ef9-1461">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1461">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f9ef9-1462">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1462">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f9ef9-1463">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1463">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f9ef9-1464">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1464">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f9ef9-1465">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1465">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f9ef9-1466">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1466">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9ef9-1467">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1467">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9ef9-1468">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1468">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9ef9-1469">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1469">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9ef9-1470">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1470">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f9ef9-1471">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1471">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f9ef9-1472">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1472">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1473">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1473">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1474">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1474">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f9ef9-1475">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1475">New cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1476">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1476">New-AzNatGateway</span></span>
        - <span data-ttu-id="f9ef9-1477">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1477">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f9ef9-1478">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1478">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f9ef9-1479">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1479">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f9ef9-1480">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1480">Updated cmdlets</span></span>
        - <span data-ttu-id="f9ef9-1481">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1481">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f9ef9-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f9ef9-1483">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1483">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f9ef9-1484">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1484">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f9ef9-1485">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1485">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9ef9-1486">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1486">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9ef9-1487">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1487">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f9ef9-1488">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1488">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f9ef9-1489">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1489">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1490">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1491">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1491">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f9ef9-1492">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1492">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f9ef9-1493">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1493">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f9ef9-1494">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1494">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f9ef9-1495">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1495">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f9ef9-1496">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1496">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f9ef9-1497">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1497">Az.Relay</span></span>
* <span data-ttu-id="f9ef9-1498">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1498">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9ef9-1499">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1499">Az.ServiceBus</span></span>
* <span data-ttu-id="f9ef9-1500">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1500">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1501">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1501">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1502">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1502">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f9ef9-1503">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1503">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f9ef9-1504">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1504">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f9ef9-1505">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1505">New-AzStorageAccount</span></span>
* <span data-ttu-id="f9ef9-1506">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1506">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f9ef9-1507">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1507">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f9ef9-1508">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1508">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f9ef9-1509">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1509">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1510">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1510">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1511">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1511">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f9ef9-1512">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1512">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f9ef9-1513">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1513">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9ef9-1514">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1514">Highlights since the last major release</span></span>
* <span data-ttu-id="f9ef9-1515">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1515">General availability of `Az` module</span></span>
* <span data-ttu-id="f9ef9-1516">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1516">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f9ef9-1517">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1517">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f9ef9-1518">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1518">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f9ef9-1519">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1519">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9ef9-1520">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1520">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1521">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1521">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1522">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1522">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1523">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1523">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f9ef9-1524">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1524">Az.Batch</span></span>
* <span data-ttu-id="f9ef9-1525">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9ef9-1526">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1526">Az.Cdn</span></span>
* <span data-ttu-id="f9ef9-1527">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1527">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9ef9-1528">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1528">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9ef9-1529">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1529">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1530">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1531">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1531">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f9ef9-1532">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1532">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9ef9-1533">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1533">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-1534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1534">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-1535">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1535">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-1536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1536">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-1537">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1537">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9ef9-1538">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1538">Az.EventGrid</span></span>
* <span data-ttu-id="f9ef9-1539">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1539">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9ef9-1540">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1540">Az.EventHub</span></span>
* <span data-ttu-id="f9ef9-1541">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1541">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f9ef9-1542">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1542">Az.HDInsight</span></span>
* <span data-ttu-id="f9ef9-1543">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-1544">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1544">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-1545">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-1546">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1546">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-1547">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9ef9-1548">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1548">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f9ef9-1549">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1549">Az.MachineLearning</span></span>
* <span data-ttu-id="f9ef9-1550">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1550">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f9ef9-1551">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1551">Az.Media</span></span>
* <span data-ttu-id="f9ef9-1552">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1552">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-1553">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1553">Az.Monitor</span></span>
  * <span data-ttu-id="f9ef9-1554">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1554">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f9ef9-1555">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1555">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f9ef9-1556">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1556">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f9ef9-1557">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1557">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f9ef9-1558">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1558">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f9ef9-1559">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1559">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f9ef9-1560">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1560">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1561">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1562">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9ef9-1563">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1563">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f9ef9-1564">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1564">Az.NotificationHubs</span></span>
* <span data-ttu-id="f9ef9-1565">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9ef9-1566">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1566">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9ef9-1567">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f9ef9-1568">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1568">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f9ef9-1569">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1570">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1570">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1571">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1571">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9ef9-1572">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1572">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f9ef9-1573">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1573">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f9ef9-1574">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1574">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9ef9-1575">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1575">Az.RedisCache</span></span>
* <span data-ttu-id="f9ef9-1576">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1576">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1577">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1578">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1578">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1579">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1580">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1580">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f9ef9-1581">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1581">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9ef9-1582">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1582">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f9ef9-1583">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1583">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f9ef9-1584">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1584">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f9ef9-1585">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1585">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f9ef9-1586">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1586">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1587">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1588">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1588">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f9ef9-1589">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f9ef9-1590">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1590">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f9ef9-1591">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1591">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f9ef9-1592">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1592">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9ef9-1593">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1593">Highlights since the last major release</span></span>
* <span data-ttu-id="f9ef9-1594">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1594">General availability of `Az` module</span></span>
* <span data-ttu-id="f9ef9-1595">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1595">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f9ef9-1596">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1596">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f9ef9-1597">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1597">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f9ef9-1598">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1598">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9ef9-1599">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1599">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1600">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1600">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1601">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1601">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1602">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1602">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f9ef9-1603">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1603">Az.AnalysisServices</span></span>
* <span data-ttu-id="f9ef9-1604">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1604">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f9ef9-1605">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1605">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1606">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1607">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1607">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f9ef9-1608">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1608">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f9ef9-1609">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1609">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1610">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1611">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1611">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f9ef9-1612">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1612">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f9ef9-1613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1613">Az.ContainerInstance</span></span>
* <span data-ttu-id="f9ef9-1614">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1614">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-1615">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1615">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-1616">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1616">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f9ef9-1617">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1617">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1618">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1619">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1619">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f9ef9-1620">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1620">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f9ef9-1621">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1621">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f9ef9-1622">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1622">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f9ef9-1623">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1623">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f9ef9-1624">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1624">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1625">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1626">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1626">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1627">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1627">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1628">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1628">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f9ef9-1629">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1629">New-AzStorageContext</span></span>
* <span data-ttu-id="f9ef9-1630">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1630">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f9ef9-1631">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1631">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f9ef9-1632">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1632">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f9ef9-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f9ef9-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f9ef9-1635">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1635">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f9ef9-1636">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1636">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f9ef9-1637">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1637">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f9ef9-1638">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1638">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f9ef9-1639">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1639">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f9ef9-1640">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1640">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f9ef9-1641">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1641">Highlights since the last major release</span></span>
* <span data-ttu-id="f9ef9-1642">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1642">General availability of `Az` module</span></span>
* <span data-ttu-id="f9ef9-1643">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1643">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f9ef9-1644">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1644">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f9ef9-1645">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1645">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f9ef9-1646">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1646">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9ef9-1647">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1647">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1648">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1648">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1649">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1650">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1650">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f9ef9-1651">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1651">Dynamic grouping</span></span>
    * <span data-ttu-id="f9ef9-1652">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1652">Pre-Post script</span></span>
    * <span data-ttu-id="f9ef9-1653">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1653">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1654">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1655">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1655">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f9ef9-1656">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1656">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-1657">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1657">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-1658">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1658">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1659">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1659">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1660">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1660">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f9ef9-1661">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1661">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1662">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1662">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1663">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1663">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f9ef9-1664">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1664">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1665">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1666">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1666">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f9ef9-1667">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1667">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1668">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1669">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1669">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1670">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1671">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1671">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f9ef9-1672">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1672">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f9ef9-1673">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1673">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f9ef9-1674">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1674">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f9ef9-1675">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1675">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f9ef9-1676">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1676">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f9ef9-1677">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1677">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1678">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1679">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1679">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f9ef9-1680">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1680">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1681">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1682">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1682">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f9ef9-1683">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1683">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1684">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1685">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1685">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f9ef9-1686">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1686">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f9ef9-1687">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1687">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9ef9-1688">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1688">Az.Cdn</span></span>
* <span data-ttu-id="f9ef9-1689">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1689">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1690">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1690">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1691">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1691">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-1692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1692">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-1693">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1693">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9ef9-1694">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1694">Az.LogicApp</span></span>
* <span data-ttu-id="f9ef9-1695">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1695">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1696">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1697">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1697">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1698">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1698">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1699">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1699">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f9ef9-1700">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1700">SDK Update</span></span>
* <span data-ttu-id="f9ef9-1701">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1701">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f9ef9-1702">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1702">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1703">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1704">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1704">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f9ef9-1705">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1705">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f9ef9-1706">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1706">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f9ef9-1707">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1707">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f9ef9-1708">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1708">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f9ef9-1709">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1709">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1710">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1711">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1711">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f9ef9-1712">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1712">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1713">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1713">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1714">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1714">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f9ef9-1715">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1715">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f9ef9-1716">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1716">Az.AnalysisServices</span></span>
* <span data-ttu-id="f9ef9-1717">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1717">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1718">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1718">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1719">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1719">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f9ef9-1720">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1720">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f9ef9-1721">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1721">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9ef9-1722">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1722">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9ef9-1723">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1723">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1724">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1725">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1725">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f9ef9-1726">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1726">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f9ef9-1727">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1727">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f9ef9-1728">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1728">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-1729">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1729">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-1730">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1730">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f9ef9-1731">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1731">Az.EventHub</span></span>
* <span data-ttu-id="f9ef9-1732">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1732">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-1733">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1733">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-1734">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1734">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9ef9-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1735">Az.LogicApp</span></span>
* <span data-ttu-id="f9ef9-1736">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1736">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f9ef9-1737">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1737">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f9ef9-1738">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1738">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f9ef9-1739">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1739">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f9ef9-1740">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1740">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f9ef9-1741">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1741">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f9ef9-1742">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1742">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f9ef9-1743">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1743">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f9ef9-1744">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1744">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f9ef9-1745">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1745">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f9ef9-1746">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1746">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f9ef9-1747">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1747">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f9ef9-1748">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1748">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f9ef9-1749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1749">Az.Monitor</span></span>
* <span data-ttu-id="f9ef9-1750">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1750">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1751">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1751">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1752">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1752">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f9ef9-1753">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1753">Az.OperationalInsights</span></span>
* <span data-ttu-id="f9ef9-1754">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1754">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f9ef9-1755">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1755">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f9ef9-1756">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1756">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1757">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1757">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1758">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1758">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f9ef9-1759">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1759">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f9ef9-1760">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1760">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f9ef9-1761">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1761">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1762">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1762">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1763">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1763">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f9ef9-1764">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1764">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1765">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1765">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1766">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1766">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f9ef9-1767">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1767">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1768">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1768">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1769">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1769">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f9ef9-1770">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1770">Az.AnalysisServices</span></span>
<span data-ttu-id="f9ef9-1771">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1771">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1772">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1773">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1773">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f9ef9-1774">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1774">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f9ef9-1775">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1775">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1776">Az.RecoveryServices</span></span>
<span data-ttu-id="f9ef9-1777">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1777">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1778">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1779">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1779">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f9ef9-1780">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1780">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f9ef9-1781">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1781">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f9ef9-1782">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1782">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1783">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1784">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1784">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f9ef9-1785">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1785">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f9ef9-1786">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1786">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f9ef9-1787">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1787">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1788">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1789">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1789">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f9ef9-1790">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1790">Az.AnalysisServices</span></span>
* <span data-ttu-id="f9ef9-1791">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1791">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1792">Az.RecoveryServices</span></span>
* <span data-ttu-id="f9ef9-1793">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1793">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f9ef9-1794">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1794">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1795">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1796">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1796">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f9ef9-1797">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1797">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9ef9-1798">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1798">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f9ef9-1799">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1799">Az.Aks</span></span>
* <span data-ttu-id="f9ef9-1800">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1800">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f9ef9-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1801">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-1802">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1802">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f9ef9-1803">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1803">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f9ef9-1804">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1804">Az.Cdn</span></span>
* <span data-ttu-id="f9ef9-1805">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1805">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1806">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1807">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1807">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f9ef9-1808">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1808">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f9ef9-1809">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1809">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f9ef9-1810">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1810">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f9ef9-1811">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1811">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f9ef9-1812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1812">Az.DataFactory</span></span>
* <span data-ttu-id="f9ef9-1813">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1813">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-1814">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1814">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-1815">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1815">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f9ef9-1816">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1816">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f9ef9-1817">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1817">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-1818">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1818">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-1819">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1819">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-1820">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1820">Az.KeyVault</span></span>
* <span data-ttu-id="f9ef9-1821">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1821">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1822">Az.Network</span></span>
* <span data-ttu-id="f9ef9-1823">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1823">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1824">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1825">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1825">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f9ef9-1826">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1826">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f9ef9-1827">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1827">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f9ef9-1828">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1828">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f9ef9-1829">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1829">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f9ef9-1830">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1830">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f9ef9-1831">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1831">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-1832">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1832">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-1833">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1833">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f9ef9-1834">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1834">Fix some error messages.</span></span>
* <span data-ttu-id="f9ef9-1835">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1835">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f9ef9-1836">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1836">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f9ef9-1837">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1837">Az.SignalR</span></span>
* <span data-ttu-id="f9ef9-1838">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1838">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1839">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1839">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1840">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1840">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9ef9-1841">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1841">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f9ef9-1842">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1842">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f9ef9-1843">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1843">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1844">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1844">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1845">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9ef9-1846">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1846">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f9ef9-1847">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1847">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f9ef9-1848">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1848">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f9ef9-1849">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1849">Az.TrafficManager</span></span>
* <span data-ttu-id="f9ef9-1850">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1850">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1851">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1851">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1852">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1852">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f9ef9-1853">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1853">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f9ef9-1854">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1854">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f9ef9-1855">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1855">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1856">Az.Accounts</span></span>
* <span data-ttu-id="f9ef9-1857">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1857">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-1858">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1858">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-1859">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1859">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f9ef9-1860">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1860">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f9ef9-1861">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1861">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-1862">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1862">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-1863">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1863">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f9ef9-1864">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1864">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f9ef9-1865">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1865">Az.EventGrid</span></span>
* <span data-ttu-id="f9ef9-1866">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1866">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f9ef9-1867">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1867">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f9ef9-1868">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1868">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f9ef9-1869">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1869">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f9ef9-1870">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1870">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f9ef9-1871">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1871">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f9ef9-1872">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1872">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f9ef9-1873">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1873">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f9ef9-1874">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1874">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f9ef9-1875">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1875">Dead letter endpoint.</span></span>
* <span data-ttu-id="f9ef9-1876">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1876">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f9ef9-1877">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1877">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f9ef9-1878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1878">Az.IotHub</span></span>
* <span data-ttu-id="f9ef9-1879">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1879">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f9ef9-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1880">Az.LogicApp</span></span>
* <span data-ttu-id="f9ef9-1881">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1881">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-1882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1882">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-1883">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1883">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f9ef9-1884">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1884">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f9ef9-1885">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1885">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f9ef9-1886">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1886">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f9ef9-1887">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1887">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f9ef9-1888">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1888">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f9ef9-1889">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1889">Az.SignalR</span></span>
* <span data-ttu-id="f9ef9-1890">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1890">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1891">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-1892">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1892">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f9ef9-1893">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1893">Az.Storage</span></span>
* <span data-ttu-id="f9ef9-1894">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1894">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f9ef9-1895">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1895">New-AzStorageContext</span></span>
* <span data-ttu-id="f9ef9-1896">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1896">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f9ef9-1897">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1897">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1898">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1898">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-1899">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1899">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f9ef9-1900">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1900">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f9ef9-1901">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1901">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f9ef9-1902">Genel</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1902">General</span></span>

- <span data-ttu-id="f9ef9-1903">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1903">General Availability of Az Module</span></span>
- <span data-ttu-id="f9ef9-1904">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1904">Online help for each module</span></span>
- <span data-ttu-id="f9ef9-1905">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1905">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f9ef9-1906">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1906">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f9ef9-1907">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1907">Az.Accounts</span></span>
- <span data-ttu-id="f9ef9-1908">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1908">Changed from Az.Profile</span></span>
- <span data-ttu-id="f9ef9-1909">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1909">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-1910">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1910">Az.ApiManagement</span></span>
- <span data-ttu-id="f9ef9-1911">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1911">Fixes for #7002</span></span>
- <span data-ttu-id="f9ef9-1912">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1912">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f9ef9-1913">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1913">Az.Batch</span></span>
- <span data-ttu-id="f9ef9-1914">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1914">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f9ef9-1915">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1915">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f9ef9-1916">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1916">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f9ef9-1917">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1917">Az.Billing</span></span>
- <span data-ttu-id="f9ef9-1918">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1918">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f9ef9-1919">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1919">Az.CognitivServices</span></span>
- <span data-ttu-id="f9ef9-1920">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1920">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f9ef9-1921">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1921">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f9ef9-1922">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1922">Az.ContainerInstance</span></span>
- <span data-ttu-id="f9ef9-1923">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1923">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f9ef9-1924">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1924">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f9ef9-1925">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1925">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-1926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1926">Az.DataLakeStore</span></span>
- <span data-ttu-id="f9ef9-1927">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1927">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f9ef9-1928">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1928">Az.Monitor</span></span>
- <span data-ttu-id="f9ef9-1929">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1929">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f9ef9-1930">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1930">Az.KeyVault</span></span>
- <span data-ttu-id="f9ef9-1931">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1931">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f9ef9-1932">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1932">Az.MachineLearning</span></span>
- <span data-ttu-id="f9ef9-1933">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1933">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f9ef9-1934">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1934">Az.Media</span></span>
- <span data-ttu-id="f9ef9-1935">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1935">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f9ef9-1936">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1936">Az.Network</span></span>
<span data-ttu-id="f9ef9-1937">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1937">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f9ef9-1938">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1938">New cmdlets added:</span></span>
        - <span data-ttu-id="f9ef9-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9ef9-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9ef9-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9ef9-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9ef9-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f9ef9-1944">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1944">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f9ef9-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f9ef9-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f9ef9-1947">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1947">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f9ef9-1948">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1948">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f9ef9-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f9ef9-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f9ef9-1951">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1951">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f9ef9-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f9ef9-1953">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1953">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f9ef9-1954">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1954">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f9ef9-1955">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1955">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f9ef9-1956">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1956">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f9ef9-1957">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1957">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f9ef9-1958">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1958">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f9ef9-1959">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1959">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f9ef9-1960">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1960">Az.OperationalInsights</span></span>
- <span data-ttu-id="f9ef9-1961">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1961">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f9ef9-1962">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1962">Az.Profile</span></span>
- <span data-ttu-id="f9ef9-1963">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1963">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1964">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1964">Az.RecoveryServices</span></span>
- <span data-ttu-id="f9ef9-1965">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1965">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f9ef9-1966">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1966">Az.Resources</span></span>
- <span data-ttu-id="f9ef9-1967">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1967">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1968">Az.ServiceFabric</span></span>
- <span data-ttu-id="f9ef9-1969">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1969">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f9ef9-1970">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1970">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f9ef9-1971">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1971">Az.SIgnalR</span></span>
- <span data-ttu-id="f9ef9-1972">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1972">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f9ef9-1973">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1973">Az.Sql</span></span>
- <span data-ttu-id="f9ef9-1974">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1974">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f9ef9-1975">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1975">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f9ef9-1976">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f9ef9-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1977">Az.Storage</span></span>
- <span data-ttu-id="f9ef9-1978">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1978">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f9ef9-1979">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1979">Az.Websites</span></span>
- <span data-ttu-id="f9ef9-1980">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1980">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f9ef9-1981">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1981">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f9ef9-1982">Genel</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1982">General</span></span>

* <span data-ttu-id="f9ef9-1983">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1983">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f9ef9-1984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1984">Az.Compute</span></span>

* <span data-ttu-id="f9ef9-1985">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1985">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-1986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1986">Az.DataLakeStore</span></span>

* <span data-ttu-id="f9ef9-1987">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1987">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f9ef9-1988">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1988">Az.FrontDoor</span></span>

* <span data-ttu-id="f9ef9-1989">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1989">Fixed some broken links</span></span>
    - <span data-ttu-id="f9ef9-1990">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1990">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f9ef9-1991">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1991">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f9ef9-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1992">Az.RecoveryServices</span></span>

* <span data-ttu-id="f9ef9-1993">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1993">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f9ef9-1994">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1994">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f9ef9-1995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1995">Az.Resources</span></span>

* <span data-ttu-id="f9ef9-1996">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1996">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f9ef9-1997">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1997">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f9ef9-1998">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1998">Az.Sql</span></span>

* <span data-ttu-id="f9ef9-1999">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="f9ef9-1999">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f9ef9-2000">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2000">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f9ef9-2001">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2001">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f9ef9-2002">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2002">Az.Storage</span></span>

* <span data-ttu-id="f9ef9-2003">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2003">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f9ef9-2004">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2004">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f9ef9-2005">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2005">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f9ef9-2006">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2006">Support Static Website configuration</span></span>
    - <span data-ttu-id="f9ef9-2007">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2007">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f9ef9-2008">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2008">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f9ef9-2009">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2009">Az.Websites</span></span>

* <span data-ttu-id="f9ef9-2010">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2010">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f9ef9-2011">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2011">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f9ef9-2012">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2012">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f9ef9-2013">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2013">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f9ef9-2014">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2014">Az.ApiManagement</span></span>
* <span data-ttu-id="f9ef9-2015">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2015">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f9ef9-2016">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2016">Az.Automation</span></span>
* <span data-ttu-id="f9ef9-2017">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2017">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f9ef9-2018">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2018">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f9ef9-2019">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2019">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f9ef9-2020">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2020">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f9ef9-2021">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2021">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f9ef9-2022">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2022">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-2023">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2023">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f9ef9-2024">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2024">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f9ef9-2025">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2025">Az.ContainerInstance</span></span>
* <span data-ttu-id="f9ef9-2026">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2026">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f9ef9-2027">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2027">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f9ef9-2028">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2028">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f9ef9-2029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2029">Az.Network</span></span>
* <span data-ttu-id="f9ef9-2030">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2030">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f9ef9-2031">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2031">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f9ef9-2032">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2032">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f9ef9-2033">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2033">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f9ef9-2034">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2034">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f9ef9-2035">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2035">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f9ef9-2036">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2036">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f9ef9-2037">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2037">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f9ef9-2038">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2038">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f9ef9-2039">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2039">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f9ef9-2040">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2040">Az.Relay</span></span>
* <span data-ttu-id="f9ef9-2041">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2041">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f9ef9-2042">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2042">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-2043">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2043">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f9ef9-2044">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2044">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f9ef9-2045">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2045">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-2046">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2046">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-2047">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2047">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f9ef9-2048">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2048">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-2049">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2049">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f9ef9-2050">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2050">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9ef9-2051">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2051">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9ef9-2052">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2052">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9ef9-2053">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2053">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f9ef9-2054">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2054">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9ef9-2055">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2055">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9ef9-2056">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2056">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f9ef9-2057">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2057">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f9ef9-2058">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2058">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f9ef9-2059">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2059">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f9ef9-2060">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2060">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f9ef9-2061">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2061">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f9ef9-2062">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2062">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f9ef9-2063">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2063">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f9ef9-2064">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2064">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f9ef9-2065">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2065">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f9ef9-2066">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2066">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f9ef9-2067">Genel</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2067">General</span></span>
* <span data-ttu-id="f9ef9-2068">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2068">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f9ef9-2069">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2069">Az.Profile</span></span>
* <span data-ttu-id="f9ef9-2070">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2070">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f9ef9-2071">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2071">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f9ef9-2072">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2072">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f9ef9-2073">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2073">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f9ef9-2074">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2074">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f9ef9-2075">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2075">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f9ef9-2076">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2076">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9ef9-2077">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2077">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9ef9-2078">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2078">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-2079">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2079">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-2080">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2080">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f9ef9-2081">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2081">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f9ef9-2082">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2082">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-2083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2083">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-2084">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2084">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f9ef9-2085">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2085">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f9ef9-2086">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2086">Az.Insights</span></span>
* <span data-ttu-id="f9ef9-2087">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2087">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f9ef9-2088">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2088">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f9ef9-2089">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2089">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f9ef9-2090">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2090">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-2091">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2091">Az.Network</span></span>
* <span data-ttu-id="f9ef9-2092">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2092">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f9ef9-2093">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2093">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f9ef9-2094">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2094">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f9ef9-2095">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2095">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f9ef9-2096">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2096">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f9ef9-2097">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2097">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f9ef9-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f9ef9-2099">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2099">Az.PolicyInsights</span></span>
* <span data-ttu-id="f9ef9-2100">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2100">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-2101">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2101">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-2102">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2102">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f9ef9-2103">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2103">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f9ef9-2104">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2104">Az.ServiceBus</span></span>
* <span data-ttu-id="f9ef9-2105">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2105">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f9ef9-2106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2106">Az.ServiceFabric</span></span>
* <span data-ttu-id="f9ef9-2107">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2107">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f9ef9-2108">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2108">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f9ef9-2109">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2109">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f9ef9-2110">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2110">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f9ef9-2111">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2111">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f9ef9-2112">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2112">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f9ef9-2113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2113">Az.Profile</span></span>
* <span data-ttu-id="f9ef9-2114">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2114">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f9ef9-2115">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2115">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-2116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2116">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-2117">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2117">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f9ef9-2118">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2118">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f9ef9-2119">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2119">Az.DataLakeStore</span></span>
* <span data-ttu-id="f9ef9-2120">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2120">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f9ef9-2121">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2121">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f9ef9-2122">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2122">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f9ef9-2123">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2123">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f9ef9-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-2125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2125">Az.Network</span></span>
* <span data-ttu-id="f9ef9-2126">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2126">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f9ef9-2127">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2127">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-2128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2128">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-2129">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2129">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f9ef9-2130">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2130">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f9ef9-2131">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2131">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f9ef9-2132">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2132">Azure.Storage</span></span>
* <span data-ttu-id="f9ef9-2133">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2133">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f9ef9-2134">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2134">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f9ef9-2135">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2135">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f9ef9-2136">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2136">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f9ef9-2137">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2137">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f9ef9-2138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2138">Az.CognitiveServices</span></span>
* <span data-ttu-id="f9ef9-2139">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2139">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f9ef9-2140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2140">Az.Compute</span></span>
* <span data-ttu-id="f9ef9-2141">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2141">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f9ef9-2142">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2142">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f9ef9-2143">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2143">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f9ef9-2144">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2144">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f9ef9-2145">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2145">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f9ef9-2146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2146">Az.Network</span></span>
* <span data-ttu-id="f9ef9-2147">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2147">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f9ef9-2148">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2148">new cmdlets added</span></span>
    - <span data-ttu-id="f9ef9-2149">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2149">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9ef9-2150">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2150">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9ef9-2151">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2151">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9ef9-2152">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2152">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f9ef9-2153">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2153">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f9ef9-2154">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2154">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f9ef9-2155">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2155">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f9ef9-2156">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2156">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f9ef9-2157">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2157">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f9ef9-2158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2158">Az.RedisCache</span></span>
* <span data-ttu-id="f9ef9-2159">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2159">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f9ef9-2160">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2160">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f9ef9-2161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2161">Az.Resources</span></span>
* <span data-ttu-id="f9ef9-2162">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2162">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f9ef9-2163">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2163">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f9ef9-2164">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2164">Az.Sql</span></span>
* <span data-ttu-id="f9ef9-2165">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2165">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f9ef9-2166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2166">Az.Websites</span></span>
* <span data-ttu-id="f9ef9-2167">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2167">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f9ef9-2168">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2168">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f9ef9-2169">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2169">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f9ef9-2170">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="f9ef9-2170">Initial Release</span></span>
