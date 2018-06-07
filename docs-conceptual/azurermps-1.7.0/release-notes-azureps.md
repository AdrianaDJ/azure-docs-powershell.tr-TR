---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9f31fe404cca1162d5e4898287261f1bcbfa0f3a
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821862"
---
# <a name="release-notes"></a><span data-ttu-id="17749-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="17749-103">Release notes</span></span>

<span data-ttu-id="17749-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="17749-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="17749-105">Sürüm 1.7.0</span><span class="sxs-lookup"><span data-stu-id="17749-105">Version 1.7.0</span></span>

* <span data-ttu-id="17749-106">**Tüm cmdlet’lerin -Force, –Confirm ve $ConfirmPreference parametreleri için davranış değişikliği. Bu uygulama PowerShell yönergelerine uygun olacak şekilde değiştirilmektedir. Çoğu cmdlet için bu durum Force parametresinin kaldırılması ve ShouldProcess isteminin atlanması anlamına gelir ve kullanıcıların ‘-Confirm:$false’ parametresini PowerShell betiklerine eklemesi gerekir.**</span><span class="sxs-lookup"><span data-stu-id="17749-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="17749-107">Bu değişiklikler aşağıdaki sorunları ele alır:</span><span class="sxs-lookup"><span data-stu-id="17749-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="17749-108">–WhatIf işlevselliğinin doğru uygulanarak kullanıcının gerçek anlamda bir değişiklik yapmadan cmdlet veya betiğin etkisini belirlemesine olanak tanıması</span><span class="sxs-lookup"><span data-stu-id="17749-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="17749-109">Olası bir değişikliğin (Cmdlet’teki ConfirmImpact ayarıyla bildirilir) etkisine göre kullanıcının uyarılabilmesi için oturum genelinde bir $ConfirmPreference kullanılarak istem üzerinde denetim</span><span class="sxs-lookup"><span data-stu-id="17749-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="17749-110">–Confirm parametresi kullanılarak onay istemleri üzerinde cmdlet’e özel denetim</span><span class="sxs-lookup"><span data-stu-id="17749-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="17749-111">Değişikliklerin özel niteliği nedeniyle kullanıcıdan istem gereken eylemler (örneğin, gizli dosyaların silinmesi) için ShouldContinue ve –Force parametresinin cmdlet’lerde tutarlı kullanımı</span><span class="sxs-lookup"><span data-stu-id="17749-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="17749-112">Diğer cmdlet’lerden alınan PowerShell betik bilgisinin Azure PowerShell cmdlet’lerine hemen uygulanabilmesi için diğer PowerShell cmdlet’leriyle tutarlılık.</span><span class="sxs-lookup"><span data-stu-id="17749-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="17749-113">**Şu anda *Tüm Durumlarda tüm İstemleri otomatik atlamak* için Azure PowerShell cmdlet’lerinin kullanıcı tarafından iki parametre girilmesini gerektirdiğini unutmayın:**</span><span class="sxs-lookup"><span data-stu-id="17749-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="17749-114">Azure İşlem</span><span class="sxs-lookup"><span data-stu-id="17749-114">Azure Compute</span></span>
  - <span data-ttu-id="17749-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="17749-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="17749-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="17749-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="17749-117">Restart-AzureVM için -Redeploy parametresi</span><span class="sxs-lookup"><span data-stu-id="17749-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="17749-118">Move-AzureService, Move-AzureStorageAccount ve Move-AzureVirtualNetwork için -Validate parametresi</span><span class="sxs-lookup"><span data-stu-id="17749-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="17749-119">Uzantı cmdlet’leri için ad ve sürüm parametreleri daha önce olduğu gibi isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="17749-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="17749-120">New-AzureVM, VM nesnesinden bir lisans türü alabilir.</span><span class="sxs-lookup"><span data-stu-id="17749-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="17749-121">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="17749-121">Azure Storage</span></span>
  - <span data-ttu-id="17749-122">Tags Parametresini Tag olarak değiştirin ve Tags parametre diğer adını ekleyin</span><span class="sxs-lookup"><span data-stu-id="17749-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="17749-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17749-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="17749-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17749-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="17749-125">Azure Ağı</span><span class="sxs-lookup"><span data-stu-id="17749-125">Azure Network</span></span>
  - <span data-ttu-id="17749-126">Sanal Ağ Eşlemesi için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="17749-127">Azure Redis Cache</span><span class="sxs-lookup"><span data-stu-id="17749-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="17749-128">Reset-AzureRmRedisCache için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="17749-129">Export-AzureRmRedisCache için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="17749-130">Import-AzureRmRedisCache için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="17749-131">New-AzureRmRedisCache cmdlet’i sanal ağ parametre değişikliğini içerecek şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="17749-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="17749-132">Azure SQL DB Yedekleme/Geri Yükleme</span><span class="sxs-lookup"><span data-stu-id="17749-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="17749-133">LTR (Uzun Süreli Saklama) yedekleme özelliği cmdlet’leri</span><span class="sxs-lookup"><span data-stu-id="17749-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="17749-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="17749-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="17749-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17749-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="17749-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="17749-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="17749-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17749-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="17749-138">Restore-AzureRmSqlDatabase artık silinmiş veritabanının bir zaman noktasına geri yüklenmesini desteklemektedir</span><span class="sxs-lookup"><span data-stu-id="17749-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="17749-139">Restore-AzureRmSqlDatabase artık Uzun Süreli Saklama yedeklemesinden geri yüklemeyi desteklemektedir</span><span class="sxs-lookup"><span data-stu-id="17749-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="17749-140">Azure LogicApp</span><span class="sxs-lookup"><span data-stu-id="17749-140">Azure LogicApp</span></span>
  - <span data-ttu-id="17749-141">LogicApp Tümleştirme hesapları cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="17749-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="17749-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="17749-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="17749-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="17749-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="17749-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="17749-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="17749-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="17749-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="17749-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17749-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="17749-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17749-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="17749-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="17749-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="17749-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="17749-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="17749-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="17749-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="17749-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="17749-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="17749-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17749-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="17749-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17749-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="17749-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="17749-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="17749-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="17749-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="17749-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="17749-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="17749-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="17749-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="17749-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17749-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="17749-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17749-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="17749-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="17749-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="17749-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="17749-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="17749-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="17749-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="17749-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="17749-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="17749-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17749-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="17749-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17749-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="17749-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="17749-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="17749-167">Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="17749-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="17749-168">Dosya ve klasörleri karşıya yükleme ve indirme performansı önemli ölçüde artırıldı.</span><span class="sxs-lookup"><span data-stu-id="17749-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="17749-169">Buna indirme parametresi adlarında küçük bir değişiklik ve karşıya yükleme için iki yeni parametrenin eklenmesi dahildir:</span><span class="sxs-lookup"><span data-stu-id="17749-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="17749-170">NumThreads -> PerFileThreadCount, tek bir dosyada kullanılacak iş parçacığı sayısını belirtmek için kullanılır</span><span class="sxs-lookup"><span data-stu-id="17749-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="17749-171">ConcurrentFileCount, klasörü karşıya yükleme/indirme işlemine paralel olarak karşıya yüklenecek/indirilecek dosya sayısını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="17749-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="17749-172">Varsayılan iş parçacığı değerleri artık çoğu dosya boyutu için tamamen daha iyi bir aktarım hızı sağlamak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="17749-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="17749-173">Performans istenen düzeyde değilse, yukarıdaki değerler gereksinimleri karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="17749-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="17749-174">Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="17749-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="17749-175">Get-AzureRMDataLakeAnalyticsDataSource artık bir bağımsız değişken olmadan çağrıldığında tüm veri kaynaklarını döndürmektedir.</span><span class="sxs-lookup"><span data-stu-id="17749-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="17749-176">Bu değişiklik, cmdlet’in veri kaynağı türü parametresini de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="17749-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="17749-177">Bu değişiklik aşağıdaki özelliklerle liste işlemi için yeni bir nesnenin döndürülmesi ile sonuçlanır:</span><span class="sxs-lookup"><span data-stu-id="17749-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="17749-178">Tür, veri kaynağının türü</span><span class="sxs-lookup"><span data-stu-id="17749-178">Type, the type of data source</span></span>
    + <span data-ttu-id="17749-179">Ad, veri kaynağının adı</span><span class="sxs-lookup"><span data-stu-id="17749-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="17749-180">IsDefault, hesabın varsayılan veri kaynağı ise true olarak ayarlanır</span><span class="sxs-lookup"><span data-stu-id="17749-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="17749-181">submittedBefore ve submittedAfter ile filtrelenirken bazı tarih saat uzaklık değerleri için Get-AzureRMDataLakeAnalyticsJob düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="17749-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="17749-182">Web Apps</span><span class="sxs-lookup"><span data-stu-id="17749-182">Web Apps</span></span>
  - <span data-ttu-id="17749-183">Düzenli takas ve önizleme ile tasar için Swap-AzureRmWebAppSlot cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="17749-184">Set-AzureRmWebAppSlot cmdlet’i otomatik takası destekleyecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="17749-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="17749-185">Azure API Management</span><span class="sxs-lookup"><span data-stu-id="17749-185">Azure API Management</span></span>
  - <span data-ttu-id="17749-186">AzureChinaCloud için Azure Api Management Dağıtımı cmdlet’leri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="17749-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="17749-187">Git Erişimi Varsayılan olarak etkin olduğundan Set-AzureRmApiManagementTenantGitAccess cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="17749-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="17749-188">Azure Kurtarma Hizmetleri Yedeklemesi</span><span class="sxs-lookup"><span data-stu-id="17749-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="17749-189">Azure SQL iş yükü için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="17749-190">Şifrelenmiş Azure VM’lerini yedeklemek ve geri yüklemek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="17749-191">Backup-AzureRmRecoveryServicesBackupItem - Kurtarma noktaları için isteğe bağlı saklama süresi özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="17749-192">Get-AzureRmRecoveryServicesBackupContainer ve Get-AzureRmRecoveryServicesBackupItem cmdlet’lerinde filtreyle ilgili küçük hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="17749-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="17749-193">Azure Otomasyonu</span><span class="sxs-lookup"><span data-stu-id="17749-193">Azure Automation</span></span>
  - <span data-ttu-id="17749-194">Get-AzureRmAutomationHybridWorkerGroup eklendi</span><span class="sxs-lookup"><span data-stu-id="17749-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
