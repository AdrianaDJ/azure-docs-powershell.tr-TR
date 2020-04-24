---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: c02cfaa7f7f39393f21cec31c5115f009381b19c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "81446062"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="1ade4-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="1ade4-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="1ade4-104">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="1ade4-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="1ade4-105">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-105">General</span></span>
* <span data-ttu-id="1ade4-106">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="1ade4-107">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="1ade4-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="1ade4-108">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1ade4-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="1ade4-109">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="1ade4-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="1ade4-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1ade4-110">Az.Billing</span></span>
  - <span data-ttu-id="1ade4-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-111">Az.Compute</span></span>
  - <span data-ttu-id="1ade4-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1ade4-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="1ade4-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-113">Az.EventHub</span></span>
  - <span data-ttu-id="1ade4-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-114">Az.IotHub</span></span>
  - <span data-ttu-id="1ade4-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-115">Az.KeyVault</span></span>
  - <span data-ttu-id="1ade4-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-116">Az.Monitor</span></span>
  - <span data-ttu-id="1ade4-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-117">Az.Network</span></span>
  - <span data-ttu-id="1ade4-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-118">Az.Resources</span></span>
  - <span data-ttu-id="1ade4-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-119">Az.Storage</span></span>
  - <span data-ttu-id="1ade4-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-120">Az.Websites</span></span>
* <span data-ttu-id="1ade4-121">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="1ade4-122">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="1ade4-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="1ade4-123">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="1ade4-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](aka.ms/InstallASHPowerShell)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-124">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-125">ADAL’den MSAL’ye yükseltme</span><span class="sxs-lookup"><span data-stu-id="1ade4-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="1ade4-126">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="1ade4-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-127">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-128">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="1ade4-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-129">Az.Compute</span></span>
* <span data-ttu-id="1ade4-130">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="1ade4-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="1ade4-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="1ade4-132">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="1ade4-133">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="1ade4-134">[#11354]</span><span class="sxs-lookup"><span data-stu-id="1ade4-134">[#11354]</span></span>
* <span data-ttu-id="1ade4-135">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="1ade4-136">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="1ade4-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1ade4-137">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="1ade4-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1ade4-138">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="1ade4-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="1ade4-139">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="1ade4-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="1ade4-140">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="1ade4-141">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="1ade4-142">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="1ade4-143">[#11257]</span><span class="sxs-lookup"><span data-stu-id="1ade4-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-144">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-145">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="1ade4-146">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-148">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="1ade4-149">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1ade4-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ade4-150">Az.HDInsight</span></span>
* <span data-ttu-id="1ade4-151">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-152">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-153">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="1ade4-154">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ade4-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="1ade4-155">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="1ade4-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="1ade4-156">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="1ade4-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-157">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-158">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-159">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-160">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-161">Az.Network</span></span>
* <span data-ttu-id="1ade4-162">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="1ade4-163">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="1ade4-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1ade4-164">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="1ade4-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="1ade4-165">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="1ade4-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="1ade4-166">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="1ade4-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="1ade4-167">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1ade4-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="1ade4-169">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-171">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="1ade4-172">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="1ade4-173">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="1ade4-174">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="1ade4-175">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="1ade4-176">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-177">Az.Resources</span></span>
* <span data-ttu-id="1ade4-178">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="1ade4-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="1ade4-179">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="1ade4-180">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="1ade4-181">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-181">Added example.</span></span>
* <span data-ttu-id="1ade4-182">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="1ade4-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="1ade4-183">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="1ade4-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-184">Az.Sql</span></span>
* <span data-ttu-id="1ade4-185">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="1ade4-186">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="1ade4-187">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="1ade4-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="1ade4-188">Az.Support</span></span>
* <span data-ttu-id="1ade4-189">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-190">Az.Websites</span></span>
* <span data-ttu-id="1ade4-191">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="1ade4-192">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="1ade4-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1ade4-193">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="1ade4-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1ade4-194">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="1ade4-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="1ade4-195">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="1ade4-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="1ade4-196">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="1ade4-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-197">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-198">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="1ade4-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="1ade4-199">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="1ade4-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="1ade4-200">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1ade4-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-201">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-202">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="1ade4-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="1ade4-203">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="1ade4-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="1ade4-204">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="1ade4-205">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="1ade4-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-207">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-208">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-209">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="1ade4-210">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ade4-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="1ade4-211">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1ade4-212">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1ade4-213">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1ade4-214">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="1ade4-215">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="1ade4-216">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ade4-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="1ade4-217">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1ade4-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="1ade4-218">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1ade4-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="1ade4-219">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1ade4-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="1ade4-220">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="1ade4-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="1ade4-221">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="1ade4-222">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="1ade4-223">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="1ade4-224">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ade4-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="1ade4-225">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="1ade4-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="1ade4-226">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="1ade4-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="1ade4-227">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-228">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-229">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="1ade4-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-230">Az.Network</span></span>
* <span data-ttu-id="1ade4-231">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="1ade4-232">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="1ade4-233">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="1ade4-234">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-235">Az.Resources</span></span>
* <span data-ttu-id="1ade4-236">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="1ade4-237">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="1ade4-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="1ade4-238">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="1ade4-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="1ade4-239">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="1ade4-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="1ade4-240">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="1ade4-241">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="1ade4-242">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="1ade4-243">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="1ade4-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ade4-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="1ade4-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ade4-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="1ade4-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ade4-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="1ade4-247">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="1ade4-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ade4-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="1ade4-249">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-250">Az.Sql</span></span>
* <span data-ttu-id="1ade4-251">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="1ade4-252">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="1ade4-253">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ade4-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="1ade4-254">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="1ade4-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="1ade4-255">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="1ade4-256">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="1ade4-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="1ade4-257">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="1ade4-258">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="1ade4-259">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-260">Az.Storage</span></span>
* <span data-ttu-id="1ade4-261">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="1ade4-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="1ade4-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="1ade4-263">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="1ade4-264">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="1ade4-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="1ade4-265">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="1ade4-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-266">Az.Websites</span></span>
* <span data-ttu-id="1ade4-267">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="1ade4-268">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="1ade4-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="1ade4-269">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="1ade4-270">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="1ade4-271">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="1ade4-272">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="1ade4-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1ade4-273">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="1ade4-273">Highlights since the last major release</span></span>
* <span data-ttu-id="1ade4-274">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="1ade4-275">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="1ade4-276">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-277">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-278">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-279">Az.Automation</span></span>
* <span data-ttu-id="1ade4-280">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1ade4-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="1ade4-282">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="1ade4-283">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-284">Az.Compute</span></span>
* <span data-ttu-id="1ade4-285">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1ade4-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1ade4-286">Az.FrontDoor</span></span>
* <span data-ttu-id="1ade4-287">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-288">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-289">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="1ade4-290">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ade4-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="1ade4-291">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1ade4-292">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1ade4-293">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="1ade4-294">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="1ade4-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-295">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-296">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-297">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-298">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="1ade4-299">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="1ade4-300">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-301">Az.Network</span></span>
* <span data-ttu-id="1ade4-302">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="1ade4-303">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="1ade4-304">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="1ade4-305">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="1ade4-306">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-306">No new cmdlets are added.</span></span> <span data-ttu-id="1ade4-307">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-309">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-310">Az.Resources</span></span>
* <span data-ttu-id="1ade4-311">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="1ade4-312">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1ade4-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="1ade4-313">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1ade4-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="1ade4-314">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="1ade4-315">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="1ade4-316">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="1ade4-317">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="1ade4-318">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-319">Az.Sql</span></span>
* <span data-ttu-id="1ade4-320">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="1ade4-321">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="1ade4-322">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="1ade4-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="1ade4-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1ade4-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="1ade4-324">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1ade4-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1ade4-325">Az.StorageSync</span></span>
* <span data-ttu-id="1ade4-326">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="1ade4-327">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="1ade4-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1ade4-328">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="1ade4-328">Highlights since the last major release</span></span>
* <span data-ttu-id="1ade4-329">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="1ade4-330">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-331">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-332">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="1ade4-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="1ade4-333">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1ade4-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-334">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-335">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="1ade4-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="1ade4-336">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="1ade4-336">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="1ade4-337">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="1ade4-338">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-339">Az.Compute</span></span>
* <span data-ttu-id="1ade4-340">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="1ade4-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="1ade4-341">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="1ade4-342">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="1ade4-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="1ade4-344">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-345">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-346">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1ade4-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1ade4-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="1ade4-348">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="1ade4-349">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1ade4-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ade4-350">Az.HDInsight</span></span>
* <span data-ttu-id="1ade4-351">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-352">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-353">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-354">Az.Network</span></span>
* <span data-ttu-id="1ade4-355">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="1ade4-356">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="1ade4-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="1ade4-357">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1ade4-358">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="1ade4-359">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="1ade4-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="1ade4-360">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="1ade4-361">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="1ade4-362">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="1ade4-363">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-363">New cmdlets added:</span></span>
        - <span data-ttu-id="1ade4-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ade4-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="1ade4-365">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="1ade4-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="1ade4-367">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1ade4-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="1ade4-369">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="1ade4-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="1ade4-370">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="1ade4-371">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="1ade4-372">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-374">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="1ade4-375">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-376">Az.Resources</span></span>
* <span data-ttu-id="1ade4-377">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="1ade4-378">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-379">Az.Sql</span></span>
<span data-ttu-id="1ade4-380">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-381">Az.Storage</span></span>
* <span data-ttu-id="1ade4-382">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="1ade4-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="1ade4-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="1ade4-384">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="1ade4-385">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-386">Az.Websites</span></span>
* <span data-ttu-id="1ade4-387">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="1ade4-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="1ade4-388">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="1ade4-389">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="1ade4-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-390">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-391">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1ade4-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1ade4-392">Az.Cdn</span></span>
* <span data-ttu-id="1ade4-393">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="1ade4-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-394">Az.Compute</span></span>
* <span data-ttu-id="1ade4-395">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="1ade4-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="1ade4-397">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="1ade4-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1ade4-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="1ade4-399">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1ade4-400">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="1ade4-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="1ade4-401">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1ade4-402">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ade4-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="1ade4-403">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1ade4-404">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="1ade4-405">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="1ade4-406">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="1ade4-407">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1ade4-408">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="1ade4-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="1ade4-409">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1ade4-410">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ade4-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="1ade4-411">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="1ade4-412">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="1ade4-413">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="1ade4-414">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="1ade4-415">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="1ade4-416">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ade4-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-417">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-418">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="1ade4-419">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="1ade4-420">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="1ade4-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="1ade4-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="1ade4-422">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1ade4-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-423">Az.EventHub</span></span>
* <span data-ttu-id="1ade4-424">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1ade4-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ade4-425">Az.HDInsight</span></span>
* <span data-ttu-id="1ade4-426">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1ade4-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1ade4-427">Az.MachineLearning</span></span>
* <span data-ttu-id="1ade4-428">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="1ade4-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1ade4-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="1ade4-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="1ade4-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="1ade4-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1ade4-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="1ade4-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1ade4-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="1ade4-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1ade4-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="1ade4-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="1ade4-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="1ade4-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="1ade4-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-436">Az.Network</span></span>
* <span data-ttu-id="1ade4-437">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-439">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="1ade4-440">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="1ade4-441">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="1ade4-442">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-443">Az.Resources</span></span>
* <span data-ttu-id="1ade4-444">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-445">Az.Sql</span></span>
* <span data-ttu-id="1ade4-446">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="1ade4-447">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="1ade4-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1ade4-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="1ade4-449">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-450">Az.Storage</span></span>
* <span data-ttu-id="1ade4-451">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="1ade4-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="1ade4-453">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="1ade4-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="1ade4-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="1ade4-455">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="1ade4-456">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-456">General</span></span>
* <span data-ttu-id="1ade4-457">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-458">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-459">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="1ade4-460">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1ade4-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1ade4-461">Az.Batch</span></span>
* <span data-ttu-id="1ade4-462">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-463">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-464">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1ade4-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1ade4-465">Az.FrontDoor</span></span>
* <span data-ttu-id="1ade4-466">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="1ade4-467">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1ade4-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1ade4-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="1ade4-469">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="1ade4-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-470">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-471">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="1ade4-472">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="1ade4-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="1ade4-473">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-474">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-475">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="1ade4-476">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="1ade4-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="1ade4-477">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="1ade4-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-478">Az.Network</span></span>
* <span data-ttu-id="1ade4-479">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-480">Az.Resources</span></span>
* <span data-ttu-id="1ade4-481">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="1ade4-482">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-483">Az.Sql</span></span>
* <span data-ttu-id="1ade4-484">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-485">Az.Storage</span></span>
* <span data-ttu-id="1ade4-486">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="1ade4-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="1ade4-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="1ade4-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1ade4-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="1ade4-489">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="1ade4-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="1ade4-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="1ade4-491">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="1ade4-492">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="1ade4-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1ade4-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="1ade4-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1ade4-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="1ade4-495">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="1ade4-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="1ade4-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="1ade4-497">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="1ade4-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="1ade4-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="1ade4-499">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1ade4-500">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="1ade4-500">Highlights since the last major release</span></span>
* <span data-ttu-id="1ade4-501">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="1ade4-502">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-503">Az.Compute</span></span>
* <span data-ttu-id="1ade4-504">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="1ade4-504">VM Reapply feature</span></span>
    - <span data-ttu-id="1ade4-505">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="1ade4-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="1ade4-506">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="1ade4-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="1ade4-507">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1ade4-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="1ade4-508">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="1ade4-509">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1ade4-510">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="1ade4-511">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="1ade4-512">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="1ade4-513">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="1ade4-514">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="1ade4-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="1ade4-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="1ade4-516">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1ade4-517">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="1ade4-517">Get the Order</span></span>
* <span data-ttu-id="1ade4-518">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1ade4-519">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="1ade4-519">Create new Order</span></span>
* <span data-ttu-id="1ade4-520">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="1ade4-521">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="1ade4-521">Remove the Order</span></span>
* <span data-ttu-id="1ade4-522">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="1ade4-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="1ade4-523">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ade4-523">Now creates Local Share</span></span>
* <span data-ttu-id="1ade4-524">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="1ade4-525">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="1ade4-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="1ade4-526">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="1ade4-527">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="1ade4-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="1ade4-528">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1ade4-529">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="1ade4-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="1ade4-530">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1ade4-531">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="1ade4-531">Create new Triggers</span></span>
* <span data-ttu-id="1ade4-532">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="1ade4-533">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="1ade4-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-534">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-535">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="1ade4-536">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-538">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1ade4-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-539">Az.EventHub</span></span>
* <span data-ttu-id="1ade4-540">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1ade4-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1ade4-541">Az.FrontDoor</span></span>
* <span data-ttu-id="1ade4-542">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="1ade4-543">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="1ade4-544">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="1ade4-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="1ade4-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-546">Az.Network</span></span>
* <span data-ttu-id="1ade4-547">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="1ade4-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="1ade4-548">Az.PrivateDns</span></span>
* <span data-ttu-id="1ade4-549">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-551">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="1ade4-552">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="1ade4-553">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1ade4-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1ade4-554">Az.RedisCache</span></span>
* <span data-ttu-id="1ade4-555">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="1ade4-556">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="1ade4-557">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-558">Az.Resources</span></span>
- <span data-ttu-id="1ade4-559">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="1ade4-560">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="1ade4-561">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="1ade4-562">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="1ade4-563">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-564">Az.Sql</span></span>
* <span data-ttu-id="1ade4-565">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="1ade4-566">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="1ade4-567">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="1ade4-568">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-568">General</span></span>
* <span data-ttu-id="1ade4-569">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-570">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-571">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1ade4-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1ade4-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1ade4-572">Az.Advisor</span></span>
* <span data-ttu-id="1ade4-573">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1ade4-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1ade4-574">Az.Batch</span></span>
* <span data-ttu-id="1ade4-575">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="1ade4-576">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="1ade4-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="1ade4-577">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="1ade4-578">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="1ade4-579">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="1ade4-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="1ade4-580">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="1ade4-581">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="1ade4-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="1ade4-582">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="1ade4-583">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="1ade4-584">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1ade4-585">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="1ade4-586">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="1ade4-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="1ade4-587">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="1ade4-588">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="1ade4-589">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="1ade4-590">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="1ade4-591">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="1ade4-592">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="1ade4-593">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="1ade4-594">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="1ade4-595">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1ade4-596">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="1ade4-597">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="1ade4-598">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="1ade4-599">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="1ade4-600">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="1ade4-601">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="1ade4-602">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="1ade4-603">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="1ade4-604">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="1ade4-605">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="1ade4-606">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="1ade4-607">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="1ade4-608">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="1ade4-609">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="1ade4-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="1ade4-610">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="1ade4-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1ade4-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1ade4-611">Az.Cdn</span></span>
* <span data-ttu-id="1ade4-612">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="1ade4-613">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-614">Az.Compute</span></span>
* <span data-ttu-id="1ade4-615">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="1ade4-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="1ade4-616">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="1ade4-617">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1ade4-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="1ade4-618">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1ade4-619">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="1ade4-620">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="1ade4-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="1ade4-621">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="1ade4-622">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1ade4-622">Breaking changes</span></span>
    - <span data-ttu-id="1ade4-623">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="1ade4-624">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="1ade4-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-625">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-626">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-628">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="1ade4-629">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="1ade4-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="1ade4-630">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="1ade4-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="1ade4-631">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="1ade4-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="1ade4-632">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="1ade4-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="1ade4-633">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="1ade4-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1ade4-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1ade4-634">Az.FrontDoor</span></span>
* <span data-ttu-id="1ade4-635">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1ade4-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ade4-636">Az.HDInsight</span></span>
* <span data-ttu-id="1ade4-637">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="1ade4-638">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="1ade4-639">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="1ade4-640">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="1ade4-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="1ade4-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1ade4-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1ade4-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1ade4-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1ade4-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="1ade4-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="1ade4-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1ade4-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="1ade4-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1ade4-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="1ade4-646">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="1ade4-647">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="1ade4-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1ade4-648">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="1ade4-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="1ade4-649">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="1ade4-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="1ade4-650">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="1ade4-651">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="1ade4-652">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="1ade4-653">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="1ade4-654">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="1ade4-655">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="1ade4-656">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="1ade4-657">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="1ade4-658">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="1ade4-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-659">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-660">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="1ade4-660">Breaking changes:</span></span>
    - <span data-ttu-id="1ade4-661">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1ade4-662">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1ade4-663">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1ade4-664">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1ade4-665">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="1ade4-666">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="1ade4-667">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="1ade4-668">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="1ade4-669">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1ade4-670">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="1ade4-671">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="1ade4-672">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-674">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="1ade4-675">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="1ade4-676">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="1ade4-677">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="1ade4-678">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="1ade4-679">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="1ade4-680">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="1ade4-681">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="1ade4-682">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-683">Az.Resources</span></span>
* <span data-ttu-id="1ade4-684">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-685">Az.Network</span></span>
* <span data-ttu-id="1ade4-686">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="1ade4-687">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="1ade4-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1ade4-693">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="1ade4-694">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1ade4-694">New cmdlet:</span></span>
        - <span data-ttu-id="1ade4-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1ade4-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="1ade4-696">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="1ade4-697">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="1ade4-698">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="1ade4-699">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="1ade4-700">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="1ade4-701">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="1ade4-702">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="1ade4-703">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-703">New cmdlets added:</span></span>
        - <span data-ttu-id="1ade4-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1ade4-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="1ade4-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1ade4-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1ade4-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="1ade4-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="1ade4-709">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="1ade4-710">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1ade4-711">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1ade4-712">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="1ade4-713">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="1ade4-714">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="1ade4-715">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="1ade4-716">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-716">New cmdlets added:</span></span>
        - <span data-ttu-id="1ade4-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="1ade4-718">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1ade4-719">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1ade4-720">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1ade4-721">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1ade4-722">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="1ade4-723">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="1ade4-724">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="1ade4-725">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-725">New cmdlets added:</span></span>
        - <span data-ttu-id="1ade4-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="1ade4-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="1ade4-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="1ade4-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="1ade4-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1ade4-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="1ade4-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="1ade4-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="1ade4-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="1ade4-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="1ade4-732">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1ade4-733">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="1ade4-734">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="1ade4-735">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="1ade4-736">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="1ade4-737">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="1ade4-738">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="1ade4-739">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="1ade4-740">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="1ade4-741">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="1ade4-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="1ade4-742">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="1ade4-743">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-743">New cmdlets added:</span></span>
        - <span data-ttu-id="1ade4-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1ade4-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="1ade4-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1ade4-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="1ade4-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1ade4-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="1ade4-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1ade4-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1ade4-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-749">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-750">Az.Sql</span></span>
* <span data-ttu-id="1ade4-751">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="1ade4-752">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="1ade4-753">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="1ade4-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="1ade4-754">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="1ade4-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="1ade4-755">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="1ade4-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="1ade4-756">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1ade4-757">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="1ade4-758">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="1ade4-759">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-760">Az.Storage</span></span>
* <span data-ttu-id="1ade4-761">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="1ade4-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1ade4-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1ade4-764">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="1ade4-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="1ade4-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1ade4-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="1ade4-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1ade4-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="1ade4-767">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="1ade4-768">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-768">General</span></span>
* <span data-ttu-id="1ade4-769">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="1ade4-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-770">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-771">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1ade4-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-772">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-773">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="1ade4-774">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-775">Az.Automation</span></span>
* <span data-ttu-id="1ade4-776">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1ade4-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1ade4-777">Az.Batch</span></span>
* <span data-ttu-id="1ade4-778">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="1ade4-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-779">Az.Compute</span></span>
* <span data-ttu-id="1ade4-780">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="1ade4-781">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="1ade4-782">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="1ade4-783">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-784">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-785">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="1ade4-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="1ade4-786">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="1ade4-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="1ade4-787">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-789">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="1ade4-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="1ade4-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="1ade4-791">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="1ade4-792">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="1ade4-793">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="1ade4-794">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-795">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-796">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="1ade4-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="1ade4-797">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-798">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-799">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="1ade4-800">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ade4-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="1ade4-801">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="1ade4-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="1ade4-802">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-803">Az.Network</span></span>
* <span data-ttu-id="1ade4-804">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="1ade4-805">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="1ade4-806">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-806">New cmdlets added:</span></span>
        - <span data-ttu-id="1ade4-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="1ade4-808">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1ade4-809">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="1ade4-810">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="1ade4-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1ade4-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1ade4-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1ade4-814">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="1ade4-815">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="1ade4-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="1ade4-816">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="1ade4-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="1ade4-817">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="1ade4-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1ade4-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1ade4-818">Az.RedisCache</span></span>
* <span data-ttu-id="1ade4-819">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-820">Az.Sql</span></span>
* <span data-ttu-id="1ade4-821">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-822">Az.Storage</span></span>
* <span data-ttu-id="1ade4-823">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="1ade4-824">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="1ade4-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1ade4-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1ade4-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="1ade4-826">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="1ade4-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="1ade4-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1ade4-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1ade4-828">Az.StorageSync</span></span>
* <span data-ttu-id="1ade4-829">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-830">Az.Websites</span></span>
* <span data-ttu-id="1ade4-831">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="1ade4-832">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1ade4-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-833">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-834">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="1ade4-835">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="1ade4-836">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ade4-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-837">Az.Automation</span></span>
* <span data-ttu-id="1ade4-838">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="1ade4-839">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="1ade4-840">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-841">Az.Compute</span></span>
* <span data-ttu-id="1ade4-842">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="1ade4-843">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1ade4-844">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="1ade4-845">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="1ade4-846">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="1ade4-847">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="1ade4-848">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="1ade4-849">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="1ade4-850">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-851">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-852">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="1ade4-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="1ade4-853">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1ade4-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ade4-854">Az.HDInsight</span></span>
* <span data-ttu-id="1ade4-855">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="1ade4-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-856">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-857">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="1ade4-858">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="1ade4-859">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ade4-859">New cmdlets are:</span></span>
    - <span data-ttu-id="1ade4-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1ade4-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1ade4-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1ade4-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1ade4-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1ade4-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="1ade4-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1ade4-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-864">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-865">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="1ade4-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="1ade4-866">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="1ade4-867">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="1ade4-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="1ade4-868">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="1ade4-868">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="1ade4-869">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="1ade4-870">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="1ade4-871">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="1ade4-872">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-872">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="1ade4-873">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1ade4-874">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="1ade4-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="1ade4-875">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="1ade4-876">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="1ade4-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="1ade4-877">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="1ade4-878">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ade4-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="1ade4-879">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ade4-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="1ade4-880">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="1ade4-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="1ade4-881">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ade4-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="1ade4-882">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="1ade4-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="1ade4-883">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="1ade4-884">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-884">Overall improved help files</span></span>
* <span data-ttu-id="1ade4-885">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-886">Az.Network</span></span>
* <span data-ttu-id="1ade4-887">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="1ade4-888">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="1ade4-889">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="1ade4-890">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="1ade4-891">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="1ade4-892">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="1ade4-893">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="1ade4-894">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="1ade4-895">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="1ade4-896">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="1ade4-897">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="1ade4-898">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="1ade4-899">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-899">New cmdlets</span></span>
        - <span data-ttu-id="1ade4-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="1ade4-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="1ade4-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="1ade4-902">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="1ade4-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="1ade4-903">New-VpnSite</span></span>
        - <span data-ttu-id="1ade4-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="1ade4-904">Update-VpnSite</span></span>
        - <span data-ttu-id="1ade4-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-905">New-VpnConnection</span></span>
        - <span data-ttu-id="1ade4-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-906">Update-VpnConnection</span></span>
* <span data-ttu-id="1ade4-907">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-909">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="1ade4-910">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-911">Az.Resources</span></span>
* <span data-ttu-id="1ade4-912">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1ade4-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-914">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="1ade4-915">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="1ade4-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="1ade4-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1ade4-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1ade4-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1ade4-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1ade4-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1ade4-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1ade4-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1ade4-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="1ade4-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1ade4-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1ade4-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1ade4-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1ade4-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1ade4-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1ade4-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1ade4-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1ade4-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1ade4-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="1ade4-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1ade4-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="1ade4-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1ade4-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="1ade4-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1ade4-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="1ade4-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="1ade4-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="1ade4-929">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1ade4-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1ade4-930">Az.SignalR</span></span>
* <span data-ttu-id="1ade4-931">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-932">Az.Sql</span></span>
* <span data-ttu-id="1ade4-933">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="1ade4-934">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="1ade4-935">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="1ade4-936">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="1ade4-937">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-938">Az.Storage</span></span>
* <span data-ttu-id="1ade4-939">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="1ade4-940">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="1ade4-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="1ade4-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="1ade4-943">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="1ade4-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="1ade4-945">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="1ade4-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1ade4-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1ade4-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1ade4-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1ade4-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1ade4-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="1ade4-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="1ade4-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-950">Az.Websites</span></span>
* <span data-ttu-id="1ade4-951">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="1ade4-952">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="1ade4-953">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="1ade4-954">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="1ade4-955">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-955">General</span></span>
* <span data-ttu-id="1ade4-956">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-957">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-958">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="1ade4-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="1ade4-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1ade4-959">Az.Aks</span></span>
* <span data-ttu-id="1ade4-960">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="1ade4-961">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="1ade4-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1ade4-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-962">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-963">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="1ade4-964">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="1ade4-965">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="1ade4-966">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="1ade4-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="1ade4-967">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1ade4-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1ade4-968">Az.Batch</span></span>
* <span data-ttu-id="1ade4-969">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1ade4-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1ade4-970">Az.Cdn</span></span>
* <span data-ttu-id="1ade4-971">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-972">Az.Compute</span></span>
* <span data-ttu-id="1ade4-973">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="1ade4-974">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="1ade4-975">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="1ade4-976">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="1ade4-977">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="1ade4-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="1ade4-978">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="1ade4-979">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="1ade4-980">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-981">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-982">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="1ade4-983">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="1ade4-984">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="1ade4-985">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-987">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1ade4-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-988">Az.EventHub</span></span>
* <span data-ttu-id="1ade4-989">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="1ade4-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="1ade4-990">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="1ade4-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="1ade4-991">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="1ade4-992">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="1ade4-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="1ade4-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1ade4-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1ade4-994">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-995">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-996">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-997">Az.Network</span></span>
* <span data-ttu-id="1ade4-998">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="1ade4-999">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="1ade4-1000">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="1ade4-1001">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="1ade4-1002">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="1ade4-1003">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="1ade4-1004">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1ade4-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="1ade4-1006">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="1ade4-1007">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1007">Added example</span></span>
    - <span data-ttu-id="1ade4-1008">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="1ade4-1009">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="1ade4-1010">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1012">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1013">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1014">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="1ade4-1015">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="1ade4-1016">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="1ade4-1017">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1ade4-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1ade4-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="1ade4-1019">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="1ade4-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="1ade4-1020">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="1ade4-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="1ade4-1021">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1ade4-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-1023">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="1ade4-1024">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="1ade4-1025">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="1ade4-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="1ade4-1026">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="1ade4-1027">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="1ade4-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="1ade4-1028">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1029">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1030">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1031">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1032">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="1ade4-1033">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="1ade4-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="1ade4-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="1ade4-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="1ade4-1036">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="1ade4-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1038">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1039">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="1ade4-1040">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1041">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1042">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="1ade4-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="1ade4-1044">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1045">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1046">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1ade4-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="1ade4-1048">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1049">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1050">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1ade4-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1ade4-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1ade4-1052">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="1ade4-1053">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="1ade4-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-1054">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-1055">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="1ade4-1056">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1ade4-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1057">Az.EventHub</span></span>
* <span data-ttu-id="1ade4-1058">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1ade4-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1ade4-1059">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-1060">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-1061">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1ade4-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1ade4-1062">Az.LogicApp</span></span>
* <span data-ttu-id="1ade4-1063">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="1ade4-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="1ade4-1064">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="1ade4-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="1ade4-1066">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1067">Az.Network</span></span>
* <span data-ttu-id="1ade4-1068">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="1ade4-1069">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1069">New cmdlets</span></span>
        - <span data-ttu-id="1ade4-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ade4-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1ade4-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1ade4-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1ade4-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1ade4-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="1ade4-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="1ade4-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1ade4-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="1ade4-1078">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="1ade4-1079">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="1ade4-1080">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="1ade4-1081">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="1ade4-1082">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="1ade4-1083">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="1ade4-1084">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="1ade4-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1ade4-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1ade4-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1ade4-1088">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1ade4-1089">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="1ade4-1090">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="1ade4-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1ade4-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1ade4-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="1ade4-1094">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="1ade4-1095">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="1ade4-1096">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1ade4-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="1ade4-1098">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="1ade4-1099">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1101">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1ade4-1102">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="1ade4-1103">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="1ade4-1104">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1ade4-1105">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="1ade4-1106">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1ade4-1107">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="1ade4-1108">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1ade4-1109">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="1ade4-1110">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1111">Az.Resources</span></span>
- <span data-ttu-id="1ade4-1112">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="1ade4-1113">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1ade4-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1ade4-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="1ade4-1115">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1ade4-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1ade4-1116">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1117">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1118">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="1ade4-1119">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="1ade4-1120">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1121">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1122">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1ade4-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1ade4-1123">Az.StorageSync</span></span>
* <span data-ttu-id="1ade4-1124">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="1ade4-1125">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1126">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1127">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="1ade4-1128">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="1ade4-1129">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="1ade4-1130">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1131">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1132">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="1ade4-1133">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="1ade4-1134">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1ade4-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1135">Az.Advisor</span></span>
* <span data-ttu-id="1ade4-1136">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="1ade4-1137">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="1ade4-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1ade4-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-1139">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="1ade4-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1ade4-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="1ade4-1141">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="1ade4-1142">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="1ade4-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="1ade4-1143">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="1ade4-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="1ade4-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1ade4-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="1ade4-1145">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1146">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1147">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1148">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1149">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-1150">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-1151">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1ade4-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1ade4-1152">Az.EventGrid</span></span>
* <span data-ttu-id="1ade4-1153">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1154">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-1155">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1156">Az.Network</span></span>
* <span data-ttu-id="1ade4-1157">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="1ade4-1158">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1ade4-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="1ade4-1160">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="1ade4-1161">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="1ade4-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1ade4-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="1ade4-1163">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1165">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1166">Az.Resources</span></span>
    - <span data-ttu-id="1ade4-1167">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="1ade4-1168">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="1ade4-1169">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="1ade4-1170">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1ade4-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1ade4-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="1ade4-1172">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1173">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1174">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="1ade4-1175">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="1ade4-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1ade4-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1ade4-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1ade4-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1ade4-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1ade4-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1ade4-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1ade4-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1ade4-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1ade4-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1ade4-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1ade4-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="1ade4-1182">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1183">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1184">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="1ade4-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1ade4-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="1ade4-1186">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="1ade4-1187">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="1ade4-1188">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="1ade4-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1ade4-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1ade4-1191">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="1ade4-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1ade4-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="1ade4-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1ade4-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1ade4-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1ade4-1194">Az.StorageSync</span></span>
* <span data-ttu-id="1ade4-1195">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="1ade4-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="1ade4-1196">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1197">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1198">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="1ade4-1199">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="1ade4-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="1ade4-1200">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="1ade4-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1ade4-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="1ade4-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="1ade4-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1203">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1204">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="1ade4-1205">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="1ade4-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1ade4-1206">Az.Dns</span></span>
* <span data-ttu-id="1ade4-1207">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1ade4-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1ade4-1208">Az.EventGrid</span></span>
* <span data-ttu-id="1ade4-1209">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="1ade4-1210">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1210">New cmdlets:</span></span>
    - <span data-ttu-id="1ade4-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1ade4-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1ade4-1212">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1ade4-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1ade4-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1ade4-1214">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="1ade4-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1ade4-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1ade4-1216">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1ade4-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1ade4-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1ade4-1218">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1ade4-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1ade4-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1ade4-1220">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="1ade4-1221">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1ade4-1222">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="1ade4-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1ade4-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="1ade4-1224">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="1ade4-1225">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1ade4-1226">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="1ade4-1227">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="1ade4-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="1ade4-1229">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1ade4-1230">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1ade4-1231">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="1ade4-1232">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="1ade4-1233">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="1ade4-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="1ade4-1234">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="1ade4-1235">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="1ade4-1236">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="1ade4-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="1ade4-1238">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="1ade4-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1ade4-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="1ade4-1240">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="1ade4-1241">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1ade4-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="1ade4-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1ade4-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="1ade4-1244">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="1ade4-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1ade4-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="1ade4-1246">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1247">Az.Network</span></span>
* <span data-ttu-id="1ade4-1248">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="1ade4-1249">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1249">New cmdlets</span></span>
        - <span data-ttu-id="1ade4-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1ade4-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="1ade4-1251">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="1ade4-1252">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1252">New cmdlets</span></span>
        - <span data-ttu-id="1ade4-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="1ade4-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="1ade4-1254">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="1ade4-1255">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1255">New cmdlets</span></span>
        - <span data-ttu-id="1ade4-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1ade4-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1ade4-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1ade4-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1ade4-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1ade4-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1ade4-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="1ade4-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1ade4-1261">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="1ade4-1262">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1262">New cmdlets</span></span>
        - <span data-ttu-id="1ade4-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ade4-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1ade4-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ade4-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1ade4-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ade4-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1ade4-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="1ade4-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="1ade4-1267">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="1ade4-1268">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="1ade4-1269">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="1ade4-1270">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="1ade4-1271">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="1ade4-1272">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="1ade4-1273">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="1ade4-1274">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="1ade4-1275">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="1ade4-1276">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="1ade4-1277">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="1ade4-1278">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="1ade4-1279">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="1ade4-1280">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="1ade4-1281">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1ade4-1282">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="1ade4-1283">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="1ade4-1284">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ade4-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="1ade4-1285">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1ade4-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="1ade4-1286">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="1ade4-1287">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1ade4-1288">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1ade4-1289">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1ade4-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="1ade4-1291">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1292">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1293">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="1ade4-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="1ade4-1294">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1ade4-1295">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1ade4-1296">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1ade4-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-1298">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1299">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1300">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="1ade4-1301">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="1ade4-1302">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="1ade4-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1ade4-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1ade4-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1ade4-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1ade4-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1ade4-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1ade4-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1ade4-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="1ade4-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1ade4-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1308">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1309">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="1ade4-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="1ade4-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="1ade4-1311">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="1ade4-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1313">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1314">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="1ade4-1315">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="1ade4-1316">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="1ade4-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1ade4-1317">Az.Cdn</span></span>
* <span data-ttu-id="1ade4-1318">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1319">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1320">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="1ade4-1321">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1ade4-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1ade4-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1322">Az.EventHub</span></span>
* <span data-ttu-id="1ade4-1323">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="1ade4-1324">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1325">Az.Network</span></span>
* <span data-ttu-id="1ade4-1326">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="1ade4-1327">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1ade4-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="1ade4-1329">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1331">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1ade4-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1ade4-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="1ade4-1333">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1ade4-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-1335">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="1ade4-1336">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1337">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1338">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="1ade4-1339">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1ade4-1340">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="1ade4-1341">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1342">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1343">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="1ade4-1344">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1ade4-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-1346">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="1ade4-1347">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="1ade4-1348">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ade4-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="1ade4-1349">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ade4-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="1ade4-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="1ade4-1351">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ade4-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="1ade4-1352">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="1ade4-1353">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="1ade4-1354">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="1ade4-1355">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="1ade4-1356">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ade4-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="1ade4-1357">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="1ade4-1358">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="1ade4-1359">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="1ade4-1360">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ade4-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="1ade4-1361">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="1ade4-1362">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="1ade4-1363">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="1ade4-1364">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="1ade4-1365">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="1ade4-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="1ade4-1366">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="1ade4-1367">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="1ade4-1368">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="1ade4-1369">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="1ade4-1370">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="1ade4-1371">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="1ade4-1372">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="1ade4-1373">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="1ade4-1374">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="1ade4-1375">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="1ade4-1376">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="1ade4-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="1ade4-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="1ade4-1378">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="1ade4-1379">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1ade4-1380">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="1ade4-1381">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="1ade4-1382">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="1ade4-1383">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="1ade4-1384">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="1ade4-1385">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1ade4-1386">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1ade4-1387">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1ade4-1388">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="1ade4-1389">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="1ade4-1390">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1ade4-1391">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1ade4-1392">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1ade4-1393">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="1ade4-1394">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="1ade4-1395">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="1ade4-1396">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="1ade4-1397">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="1ade4-1398">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="1ade4-1399">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="1ade4-1400">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="1ade4-1401">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="1ade4-1402">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1ade4-1403">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1ade4-1404">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1ade4-1405">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1ade4-1406">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1ade4-1407">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1ade4-1408">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="1ade4-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1ade4-1409">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1ade4-1410">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="1ade4-1411">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="1ade4-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="1ade4-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="1ade4-1413">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="1ade4-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="1ade4-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="1ade4-1415">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="1ade4-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="1ade4-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="1ade4-1417">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="1ade4-1418">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="1ade4-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="1ade4-1420">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="1ade4-1421">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="1ade4-1422">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="1ade4-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1423">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1424">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="1ade4-1425">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="1ade4-1426">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="1ade4-1427">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="1ade4-1428">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="1ade4-1429">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="1ade4-1430">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1431">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1432">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="1ade4-1433">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-1435">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1436">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-1437">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1438">Az.Network</span></span>
* <span data-ttu-id="1ade4-1439">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="1ade4-1440">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="1ade4-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="1ade4-1442">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1443">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1444">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1445">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1446">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="1ade4-1447">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1448">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1449">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="1ade4-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1ade4-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="1ade4-1451">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="1ade4-1452">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1453">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1454">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="1ade4-1455">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1ade4-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="1ade4-1456">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="1ade4-1457">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="1ade4-1458">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="1ade4-1459">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="1ade4-1460">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1460">Breaking changes</span></span>
    - <span data-ttu-id="1ade4-1461">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="1ade4-1462">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1ade4-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1ade4-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="1ade4-1464">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="1ade4-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1ade4-1465">Az.Dns</span></span>
* <span data-ttu-id="1ade4-1466">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="1ade4-1467">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="1ade4-1468">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1ade4-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="1ade4-1470">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="1ade4-1471">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="1ade4-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="1ade4-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ade4-1472">Az.HDInsight</span></span>
* <span data-ttu-id="1ade4-1473">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="1ade4-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1ade4-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="1ade4-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1ade4-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1ade4-1476">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1ade4-1477">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="1ade4-1478">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="1ade4-1479">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1480">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-1481">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="1ade4-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="1ade4-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="1ade4-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="1ade4-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="1ade4-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="1ade4-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="1ade4-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="1ade4-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="1ade4-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="1ade4-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="1ade4-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="1ade4-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1ade4-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1ade4-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1ade4-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1ade4-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1ade4-1493">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1493">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="1ade4-1494">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1495">Az.Network</span></span>
* <span data-ttu-id="1ade4-1496">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="1ade4-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="1ade4-1497">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1497">New cmdlets</span></span>
        - <span data-ttu-id="1ade4-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1ade4-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="1ade4-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1ade4-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="1ade4-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1ade4-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="1ade4-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1ade4-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="1ade4-1502">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="1ade4-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1ade4-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="1ade4-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1ade4-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="1ade4-1505">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="1ade4-1506">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="1ade4-1507">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1ade4-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="1ade4-1509">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="1ade4-1510">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="1ade4-1511">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1513">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="1ade4-1514">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="1ade4-1515">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="1ade4-1516">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="1ade4-1517">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="1ade4-1518">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="1ade4-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1ade4-1519">Az.Relay</span></span>
* <span data-ttu-id="1ade4-1520">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="1ade4-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1ade4-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1ade4-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="1ade4-1522">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1523">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1524">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="1ade4-1525">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="1ade4-1526">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="1ade4-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="1ade4-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="1ade4-1528">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="1ade4-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="1ade4-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="1ade4-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="1ade4-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1532">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1533">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="1ade4-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="1ade4-1534">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="1ade4-1535">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1ade4-1536">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="1ade4-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="1ade4-1537">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="1ade4-1538">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1ade4-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1ade4-1539">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1ade4-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1ade4-1540">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1ade4-1541">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1ade4-1542">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1ade4-1543">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1544">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1545">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1ade4-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1ade4-1546">Az.Batch</span></span>
* <span data-ttu-id="1ade4-1547">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1ade4-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1ade4-1548">Az.Cdn</span></span>
* <span data-ttu-id="1ade4-1549">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1ade4-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="1ade4-1551">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1552">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1553">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="1ade4-1554">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1ade4-1555">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-1556">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-1557">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-1559">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1ade4-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1ade4-1560">Az.EventGrid</span></span>
* <span data-ttu-id="1ade4-1561">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1ade4-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1562">Az.EventHub</span></span>
* <span data-ttu-id="1ade4-1563">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="1ade4-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1ade4-1564">Az.HDInsight</span></span>
* <span data-ttu-id="1ade4-1565">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1566">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-1567">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-1568">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-1569">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1ade4-1570">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1ade4-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1ade4-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="1ade4-1572">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="1ade4-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1ade4-1573">Az.Media</span></span>
* <span data-ttu-id="1ade4-1574">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1575">Az.Monitor</span></span>
  * <span data-ttu-id="1ade4-1576">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="1ade4-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="1ade4-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="1ade4-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="1ade4-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="1ade4-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1ade4-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1ade4-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1ade4-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1ade4-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1ade4-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="1ade4-1582">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1583">Az.Network</span></span>
* <span data-ttu-id="1ade4-1584">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1ade4-1585">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="1ade4-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1ade4-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="1ade4-1587">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1ade4-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="1ade4-1589">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="1ade4-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1ade4-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="1ade4-1591">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1593">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1ade4-1594">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="1ade4-1595">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="1ade4-1596">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1ade4-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1ade4-1597">Az.RedisCache</span></span>
* <span data-ttu-id="1ade4-1598">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1599">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1600">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1601">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1602">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="1ade4-1603">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1ade4-1604">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="1ade4-1605">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="1ade4-1606">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="1ade4-1607">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="1ade4-1608">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1609">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1610">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="1ade4-1611">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1ade4-1612">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="1ade4-1613">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="1ade4-1614">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1ade4-1615">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="1ade4-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="1ade4-1616">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="1ade4-1617">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1ade4-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1ade4-1618">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1ade4-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1ade4-1619">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1ade4-1620">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1ade4-1621">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1ade4-1622">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1623">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1624">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1ade4-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="1ade4-1626">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="1ade4-1627">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="1ade4-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1628">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1629">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="1ade4-1630">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="1ade4-1631">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1632">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1633">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1ade4-1634">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="1ade4-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="1ade4-1636">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-1637">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-1638">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="1ade4-1639">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1640">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1641">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="1ade4-1642">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1ade4-1643">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="1ade4-1644">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1ade4-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="1ade4-1645">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="1ade4-1646">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1ade4-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1647">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1648">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1649">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1650">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="1ade4-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="1ade4-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ade4-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="1ade4-1652">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="1ade4-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1ade4-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1ade4-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1ade4-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1ade4-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="1ade4-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="1ade4-1657">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="1ade4-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1ade4-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1ade4-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="1ade4-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1ade4-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="1ade4-1662">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1ade4-1663">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="1ade4-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="1ade4-1664">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="1ade4-1665">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1ade4-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1ade4-1666">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1ade4-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1ade4-1667">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1ade4-1668">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1ade4-1669">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1ade4-1670">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1671">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1672">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="1ade4-1673">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="1ade4-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="1ade4-1674">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="1ade4-1674">Pre-Post script</span></span>
    * <span data-ttu-id="1ade4-1675">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1676">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1677">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="1ade4-1678">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-1679">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-1680">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1681">Az.Network</span></span>
* <span data-ttu-id="1ade4-1682">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="1ade4-1683">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1685">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="1ade4-1686">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1687">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1688">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="1ade4-1689">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1690">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1691">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1692">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1693">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="1ade4-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1ade4-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1ade4-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1ade4-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="1ade4-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="1ade4-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1ade4-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="1ade4-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1700">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1701">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="1ade4-1702">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1703">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1704">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="1ade4-1705">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1706">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1707">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="1ade4-1708">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="1ade4-1709">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="1ade4-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1ade4-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1ade4-1710">Az.Cdn</span></span>
* <span data-ttu-id="1ade4-1711">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1712">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1713">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-1714">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-1715">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1ade4-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1ade4-1716">Az.LogicApp</span></span>
* <span data-ttu-id="1ade4-1717">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="1ade4-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1718">Az.Network</span></span>
* <span data-ttu-id="1ade4-1719">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1721">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="1ade4-1722">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1722">SDK Update</span></span>
* <span data-ttu-id="1ade4-1723">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="1ade4-1724">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1725">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1726">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="1ade4-1727">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="1ade4-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="1ade4-1728">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="1ade4-1729">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="1ade4-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="1ade4-1730">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="1ade4-1731">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="1ade4-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1732">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1733">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="1ade4-1734">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1735">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1736">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ade4-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="1ade4-1737">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="1ade4-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="1ade4-1739">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1740">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1741">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="1ade4-1742">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="1ade4-1743">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1ade4-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="1ade4-1745">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1746">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1747">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="1ade4-1748">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="1ade4-1749">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="1ade4-1750">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-1752">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1ade4-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1753">Az.EventHub</span></span>
* <span data-ttu-id="1ade4-1754">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-1755">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-1756">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1ade4-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1ade4-1757">Az.LogicApp</span></span>
* <span data-ttu-id="1ade4-1758">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="1ade4-1759">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="1ade4-1760">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="1ade4-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1ade4-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1ade4-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1ade4-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1ade4-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1ade4-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1ade4-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1ade4-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="1ade4-1765">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="1ade4-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="1ade4-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ade4-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1ade4-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ade4-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1ade4-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ade4-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1ade4-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ade4-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="1ade4-1770">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1ade4-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1771">Az.Monitor</span></span>
* <span data-ttu-id="1ade4-1772">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1773">Az.Network</span></span>
* <span data-ttu-id="1ade4-1774">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1ade4-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="1ade4-1776">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="1ade4-1777">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="1ade4-1778">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1779">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1780">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1ade4-1781">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="1ade4-1782">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="1ade4-1783">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1784">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1785">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="1ade4-1786">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1787">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1788">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="1ade4-1789">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1790">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1791">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1ade4-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1ade4-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="1ade4-1793">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1794">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1795">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="1ade4-1796">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="1ade4-1797">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="1ade4-1799">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1800">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1801">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="1ade4-1802">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1ade4-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1ade4-1803">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="1ade4-1804">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1ade4-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1805">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ade4-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="1ade4-1807">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="1ade4-1808">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="1ade4-1809">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1810">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1811">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1ade4-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="1ade4-1813">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="1ade4-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="1ade4-1815">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="1ade4-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="1ade4-1816">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1817">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1818">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1ade4-1819">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1ade4-1820">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="1ade4-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1ade4-1821">Az.Aks</span></span>
* <span data-ttu-id="1ade4-1822">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1ade4-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-1823">Az.Automation</span></span>
* <span data-ttu-id="1ade4-1824">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="1ade4-1825">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1ade4-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1ade4-1826">Az.Cdn</span></span>
* <span data-ttu-id="1ade4-1827">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1828">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1829">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="1ade4-1830">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="1ade4-1831">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1ade4-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1ade4-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1ade4-1833">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1ade4-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ade4-1834">Az.DataFactory</span></span>
* <span data-ttu-id="1ade4-1835">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-1837">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="1ade4-1838">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="1ade4-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="1ade4-1839">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1840">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-1841">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1ade4-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-1842">Az.KeyVault</span></span>
* <span data-ttu-id="1ade4-1843">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1844">Az.Network</span></span>
* <span data-ttu-id="1ade4-1845">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1846">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1847">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="1ade4-1848">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="1ade4-1849">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="1ade4-1850">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="1ade4-1851">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="1ade4-1852">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="1ade4-1853">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="1ade4-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1ade4-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-1855">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="1ade4-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="1ade4-1856">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1856">Fix some error messages.</span></span>
* <span data-ttu-id="1ade4-1857">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="1ade4-1858">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1ade4-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1ade4-1859">Az.SignalR</span></span>
* <span data-ttu-id="1ade4-1860">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1861">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1862">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1ade4-1863">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="1ade4-1864">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="1ade4-1865">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1866">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1867">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1ade4-1868">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="1ade4-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1ade4-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="1ade4-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1ade4-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1ade4-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1ade4-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="1ade4-1872">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1873">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1874">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1ade4-1875">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="1ade4-1876">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="1ade4-1877">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="1ade4-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1ade4-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1878">Az.Accounts</span></span>
* <span data-ttu-id="1ade4-1879">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-1880">Az.Compute</span></span>
* <span data-ttu-id="1ade4-1881">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="1ade4-1882">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="1ade4-1883">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-1885">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="1ade4-1886">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1ade4-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1ade4-1887">Az.EventGrid</span></span>
* <span data-ttu-id="1ade4-1888">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="1ade4-1889">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="1ade4-1890">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1ade4-1891">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="1ade4-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1ade4-1892">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="1ade4-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1ade4-1893">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="1ade4-1894">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1ade4-1895">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="1ade4-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1ade4-1896">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="1ade4-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1ade4-1897">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="1ade4-1898">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="1ade4-1899">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1ade4-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1ade4-1900">Az.IotHub</span></span>
* <span data-ttu-id="1ade4-1901">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1ade4-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1ade4-1902">Az.LogicApp</span></span>
* <span data-ttu-id="1ade4-1903">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1904">Az.Resources</span></span>
* <span data-ttu-id="1ade4-1905">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="1ade4-1906">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="1ade4-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="1ade4-1907">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1ade4-1908">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="1ade4-1909">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="1ade4-1910">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="1ade4-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1ade4-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1ade4-1911">Az.SignalR</span></span>
* <span data-ttu-id="1ade4-1912">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1913">Az.Sql</span></span>
* <span data-ttu-id="1ade4-1914">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1ade4-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1915">Az.Storage</span></span>
* <span data-ttu-id="1ade4-1916">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="1ade4-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ade4-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="1ade4-1918">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="1ade4-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1ade4-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-1920">Az.Websites</span></span>
* <span data-ttu-id="1ade4-1921">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1ade4-1922">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="1ade4-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="1ade4-1923">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="1ade4-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="1ade4-1924">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-1924">General</span></span>

- <span data-ttu-id="1ade4-1925">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="1ade4-1926">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="1ade4-1926">Online help for each module</span></span>
- <span data-ttu-id="1ade4-1927">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="1ade4-1928">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="1ade4-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1ade4-1929">Az.Accounts</span></span>
- <span data-ttu-id="1ade4-1930">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1ade4-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="1ade4-1931">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1ade4-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="1ade4-1933">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="1ade4-1933">Fixes for #7002</span></span>
- <span data-ttu-id="1ade4-1934">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="1ade4-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1ade4-1935">Az.Batch</span></span>
- <span data-ttu-id="1ade4-1936">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="1ade4-1937">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="1ade4-1938">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="1ade4-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1ade4-1939">Az.Billing</span></span>
- <span data-ttu-id="1ade4-1940">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="1ade4-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="1ade4-1942">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="1ade4-1943">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1ade4-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="1ade4-1945">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="1ade4-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1ade4-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="1ade4-1947">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="1ade4-1949">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="1ade4-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1ade4-1950">Az.Monitor</span></span>
- <span data-ttu-id="1ade4-1951">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="1ade4-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1ade4-1952">Az.KeyVault</span></span>
- <span data-ttu-id="1ade4-1953">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="1ade4-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1ade4-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="1ade4-1955">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="1ade4-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1ade4-1956">Az.Media</span></span>
- <span data-ttu-id="1ade4-1957">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="1ade4-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1ade4-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-1958">Az.Network</span></span>
<span data-ttu-id="1ade4-1959">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="1ade4-1960">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="1ade4-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="1ade4-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1ade4-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1ade4-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1ade4-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1ade4-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1ade4-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="1ade4-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1ade4-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="1ade4-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ade4-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="1ade4-1969">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="1ade4-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ade4-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="1ade4-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1ade4-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1ade4-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1ade4-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="1ade4-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="1ade4-1975">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="1ade4-1976">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="1ade4-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ade4-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1ade4-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ade4-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1ade4-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ade4-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="1ade4-1980">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="1ade4-1981">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="1ade4-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="1ade4-1983">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="1ade4-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1ade4-1984">Az.Profile</span></span>
- <span data-ttu-id="1ade4-1985">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="1ade4-1987">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="1ade4-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-1988">Az.Resources</span></span>
- <span data-ttu-id="1ade4-1989">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1ade4-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="1ade4-1991">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="1ade4-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="1ade4-1992">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="1ade4-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1ade4-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="1ade4-1994">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="1ade4-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="1ade4-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-1995">Az.Sql</span></span>
- <span data-ttu-id="1ade4-1996">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="1ade4-1997">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="1ade4-1998">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="1ade4-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-1999">Az.Storage</span></span>
- <span data-ttu-id="1ade4-2000">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1ade4-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-2001">Az.Websites</span></span>
- <span data-ttu-id="1ade4-2002">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="1ade4-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="1ade4-2003">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="1ade4-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="1ade4-2004">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-2004">General</span></span>

* <span data-ttu-id="1ade4-2005">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1ade4-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="1ade4-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-2006">Az.Compute</span></span>

* <span data-ttu-id="1ade4-2007">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="1ade4-2009">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="1ade4-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1ade4-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="1ade4-2011">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="1ade4-2012">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="1ade4-2013">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1ade4-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="1ade4-2015">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="1ade4-2016">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="1ade4-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-2017">Az.Resources</span></span>

* <span data-ttu-id="1ade4-2018">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="1ade4-2019">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="1ade4-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-2020">Az.Sql</span></span>

* <span data-ttu-id="1ade4-2021">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1ade4-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="1ade4-2022">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="1ade4-2023">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="1ade4-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1ade4-2024">Az.Storage</span></span>

* <span data-ttu-id="1ade4-2025">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="1ade4-2026">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="1ade4-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1ade4-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1ade4-2028">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="1ade4-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1ade4-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="1ade4-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1ade4-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1ade4-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-2031">Az.Websites</span></span>

* <span data-ttu-id="1ade4-2032">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1ade4-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="1ade4-2033">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="1ade4-2034">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="1ade4-2035">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="1ade4-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1ade4-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ade4-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="1ade4-2037">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="1ade4-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="1ade4-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1ade4-2038">Az.Automation</span></span>
* <span data-ttu-id="1ade4-2039">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="1ade4-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="1ade4-2040">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="1ade4-2041">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="1ade4-2042">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="1ade4-2043">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="1ade4-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-2044">Az.Compute</span></span>
* <span data-ttu-id="1ade4-2045">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="1ade4-2046">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="1ade4-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1ade4-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="1ade4-2048">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="1ade4-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="1ade4-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1ade4-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1ade4-2050">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1ade4-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-2051">Az.Network</span></span>
* <span data-ttu-id="1ade4-2052">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="1ade4-2053">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="1ade4-2054">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="1ade4-2055">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="1ade4-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1ade4-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1ade4-2057">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="1ade4-2058">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="1ade4-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1ade4-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1ade4-2060">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="1ade4-2061">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="1ade4-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="1ade4-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1ade4-2062">Az.Relay</span></span>
* <span data-ttu-id="1ade4-2063">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="1ade4-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-2064">Az.Resources</span></span>
* <span data-ttu-id="1ade4-2065">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="1ade4-2066">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="1ade4-2067">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="1ade4-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1ade4-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-2069">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="1ade4-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-2070">Az.Sql</span></span>
* <span data-ttu-id="1ade4-2071">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="1ade4-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1ade4-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1ade4-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1ade4-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1ade4-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1ade4-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1ade4-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1ade4-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1ade4-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1ade4-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1ade4-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1ade4-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1ade4-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="1ade4-2080">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="1ade4-2081">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="1ade4-2082">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="1ade4-2083">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1ade4-2084">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1ade4-2085">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="1ade4-2086">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="1ade4-2087">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="1ade4-2088">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="1ade4-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1ade4-2089">Genel</span><span class="sxs-lookup"><span data-stu-id="1ade4-2089">General</span></span>
* <span data-ttu-id="1ade4-2090">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="1ade4-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="1ade4-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1ade4-2091">Az.Profile</span></span>
* <span data-ttu-id="1ade4-2092">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="1ade4-2093">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="1ade4-2094">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="1ade4-2095">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="1ade4-2096">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="1ade4-2097">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="1ade4-2098">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="1ade4-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="1ade4-2100">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-2101">Az.Compute</span></span>
* <span data-ttu-id="1ade4-2102">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="1ade4-2103">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="1ade4-2104">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-2106">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="1ade4-2107">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="1ade4-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="1ade4-2108">Az.Insights</span></span>
* <span data-ttu-id="1ade4-2109">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="1ade4-2110">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="1ade4-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="1ade4-2111">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="1ade4-2112">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-2113">Az.Network</span></span>
* <span data-ttu-id="1ade4-2114">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="1ade4-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="1ade4-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="1ade4-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="1ade4-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1ade4-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="1ade4-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1ade4-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ade4-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1ade4-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1ade4-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1ade4-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1ade4-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="1ade4-2122">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-2123">Az.Resources</span></span>
* <span data-ttu-id="1ade4-2124">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="1ade4-2125">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="1ade4-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1ade4-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1ade4-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="1ade4-2127">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1ade4-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ade4-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="1ade4-2129">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="1ade4-2130">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="1ade4-2131">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="1ade4-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="1ade4-2132">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="1ade4-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="1ade4-2133">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="1ade4-2134">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="1ade4-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="1ade4-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1ade4-2135">Az.Profile</span></span>
* <span data-ttu-id="1ade4-2136">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="1ade4-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="1ade4-2137">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-2138">Az.Compute</span></span>
* <span data-ttu-id="1ade4-2139">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="1ade4-2140">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1ade4-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1ade4-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="1ade4-2142">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="1ade4-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1ade4-2143">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1ade4-2144">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1ade4-2145">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1ade4-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-2147">Az.Network</span></span>
* <span data-ttu-id="1ade4-2148">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1ade4-2149">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-2150">Az.Resources</span></span>
* <span data-ttu-id="1ade4-2151">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1ade4-2152">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="1ade4-2153">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="1ade4-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1ade4-2154">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="1ade4-2154">Azure.Storage</span></span>
* <span data-ttu-id="1ade4-2155">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="1ade4-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1ade4-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1ade4-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1ade4-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1ade4-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1ade4-2158">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1ade4-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1ade4-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1ade4-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1ade4-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="1ade4-2161">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1ade4-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1ade4-2162">Az.Compute</span></span>
* <span data-ttu-id="1ade4-2163">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1ade4-2164">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="1ade4-2165">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="1ade4-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1ade4-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="1ade4-2167">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1ade4-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1ade4-2168">Az.Network</span></span>
* <span data-ttu-id="1ade4-2169">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1ade4-2170">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2170">new cmdlets added</span></span>
    - <span data-ttu-id="1ade4-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1ade4-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="1ade4-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1ade4-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="1ade4-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1ade4-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="1ade4-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1ade4-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="1ade4-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="1ade4-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1ade4-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1ade4-2177">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1ade4-2178">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="1ade4-2179">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1ade4-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1ade4-2180">Az.RedisCache</span></span>
* <span data-ttu-id="1ade4-2181">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="1ade4-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1ade4-2182">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="1ade4-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1ade4-2183">Az.Resources</span></span>
* <span data-ttu-id="1ade4-2184">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1ade4-2185">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="1ade4-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1ade4-2186">Az.Sql</span></span>
* <span data-ttu-id="1ade4-2187">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="1ade4-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1ade4-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1ade4-2188">Az.Websites</span></span>
* <span data-ttu-id="1ade4-2189">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1ade4-2190">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="1ade4-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="1ade4-2191">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="1ade4-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="1ade4-2192">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="1ade4-2192">Initial Release</span></span>
