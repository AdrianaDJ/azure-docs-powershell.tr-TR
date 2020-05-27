---
title: Az 3.0.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Az sürüm 3.0 yayınındaki Azure PowerShell’de yapılan hataya neden olan değişikliklerin bir listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: 06be35bc3573d00d90a8cf2d822ac051ab72f6bb
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387675"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="76995-103">Az 3.0.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="76995-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="76995-104">Bu belgede Az 2.0.0 ve 3.0.0 sürümleri arasındaki değişiklikler açıklanmaktadır</span><span class="sxs-lookup"><span data-stu-id="76995-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="76995-105">Az 3.0.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="76995-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="76995-106">Batch</span><span class="sxs-lookup"><span data-stu-id="76995-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="76995-107">Önceki `Az.Resources` sürümleriyle uyumsuzluk</span><span class="sxs-lookup"><span data-stu-id="76995-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="76995-108">İşlem</span><span class="sxs-lookup"><span data-stu-id="76995-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="76995-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="76995-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="76995-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="76995-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="76995-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76995-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="76995-112">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="76995-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="76995-113">Önceki `Az.Batch` sürümleriyle uyumsuzluk</span><span class="sxs-lookup"><span data-stu-id="76995-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="76995-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76995-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="76995-115">Sql</span><span class="sxs-lookup"><span data-stu-id="76995-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="76995-116">Batch</span><span class="sxs-lookup"><span data-stu-id="76995-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="76995-117">`Get-AzBatchNodeAgentSku` kaldırılıp `Get-AzBatchSupportedImage` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="76995-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="76995-118">`Get-AzBatchSupportedImage`, `Get-AzBatchNodeAgentSku` ile aynı verileri daha anlaşılır bir biçimde döndürür.</span><span class="sxs-lookup"><span data-stu-id="76995-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="76995-119">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="76995-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="76995-120">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="76995-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-121">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="76995-122">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="76995-123">Az.Resources Modülü ile Önceki Sürüm Uyumsuzluğu</span><span class="sxs-lookup"><span data-stu-id="76995-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="76995-124">‘Az.Batch’ modülü 2.0.1 sürümü, ‘Az.Resources’ modülünün önceki sürümleriyle (sürüm 1.7.0 veya daha önceki sürümler) uyumlu değildir.</span><span class="sxs-lookup"><span data-stu-id="76995-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="76995-125">Bu, ‘Az.Batch’ modülünün 2.0.1 sürümü içeri aktarıldığında ‘Az.Resources’ modülünün 1.7.0 sürümünün içeri aktarılmamasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="76995-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="76995-126">Bu sorunu düzeltmek için, ‘Az.Resources’ modülünü sürüm 1.7.1 veya sonraki bir sürüme güncelleştirin veya ‘Az’ modülünün en son sürümünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="76995-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="76995-127">İşlem</span><span class="sxs-lookup"><span data-stu-id="76995-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="76995-128">CreateOption değeri Upload olduğunda `New-AzDiskConfig` için `DiskSizeGB` yerine `UploadSizeInBytes` parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="76995-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="76995-129">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="76995-130">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="76995-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="76995-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="76995-132">`Get-AzHDInsightJobOutput` cmdlet'i depolama anahtarına ayrıntılı rol tabanlı erişimi destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="76995-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="76995-133">HDInsight Küme Operatörü, Katkıda Bulunan veya Sahip rolleri olan kullanıcılar etkilenmeyecek.</span><span class="sxs-lookup"><span data-stu-id="76995-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="76995-134">Yalnızca Okuyucu rolüne sahip kullanıcıların `DefaultStorageAccountKey` parametresini açık olarak belirtmesi gerekecek.</span><span class="sxs-lookup"><span data-stu-id="76995-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-135">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="76995-136">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="76995-137">`Add-AzHDInsightConfigValue` cmdlet’inin `Add-AzHDInsightConfigValues` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-138">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-138">Before</span></span>
<span data-ttu-id="76995-139">Kullanım dışı bırakılan diğer ad kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="76995-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="76995-140">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="76995-141">Yeni `Disable-AzHDInsightMonitoring` cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="76995-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="76995-142">Bir HDInsight kümesinde izlemeyi devre dışı bırakmak için bu cmdlet’i kullanın (`Disable-AzHDInsightOperationsManagementSuite` ve `Disable-AzHDInsightOMS` cmdlet’lerinin yerini alır).</span><span class="sxs-lookup"><span data-stu-id="76995-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="76995-143">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="76995-144">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="76995-145">Yeni `Enable-AzHDInsightMonitoring` cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="76995-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="76995-146">Bir HDInsight kümesinde izlemeyi etkinleştirmek için bu cmdlet’i kullanın (`Enable-AzHDInsightOperationsManagementSuite` ve `Enable-AzHDInsightOMS` cmdlet’lerinin yerini alır).</span><span class="sxs-lookup"><span data-stu-id="76995-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="76995-147">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="76995-148">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="76995-149">Yeni `Get-AzHDInsightMonitoring` cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="76995-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="76995-150">Bir Azure HDInsight kümesinde izleme yüklemesinin durumunu almak için bu cmdlet’i kullanın (`Get-AzHDInsightOperationsManagementSuite` ve `Get-AzHDInsightOMS` cmdlet’lerinin yerini alır).</span><span class="sxs-lookup"><span data-stu-id="76995-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="76995-151">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="76995-152">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="76995-153">`Get-HDInsightProperty` cmdlet’inin `Get-AzHDInsightProperties` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-154">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-154">Before</span></span>
<span data-ttu-id="76995-155">Kullanım dışı bırakılan diğer ad kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="76995-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="76995-156">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="76995-157">`Grant-AzHDInsightRdpServicesAccess` ve `Revoke-AzHDInsightRdpServicesAccess` cmdlet'leri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="76995-158">Windows işletim sistemi türünü kullanan kümeler desteklenmediğinden bunlar artık gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="76995-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="76995-159">Lütfen Linux işletim sistemi türünü kullanarak bir küme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="76995-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="76995-160">`Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` olan `Remove-AzHDInsightCluster` çıkış türü `bool` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="76995-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-161">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="76995-162">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="76995-163">Cmdlet kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="76995-164">Bunun için bir değişiklik yoktur.</span><span class="sxs-lookup"><span data-stu-id="76995-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="76995-165">`HttpConnectivitySettings` olan `Set-AzHDInsightGatewayCredential` çıkış türü `AzureHDInsightGatewaySettings` olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="76995-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="76995-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="76995-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="76995-167">Bu diğer ad kaldırıldı, lütfen bunun yerine `New-AzIotHubImportDevice` kullanın.</span><span class="sxs-lookup"><span data-stu-id="76995-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-168">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="76995-169">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="76995-170">Bu diğer ad kaldırıldı, lütfen bunun yerine `New-AzIotHubExportDevice` kullanın.</span><span class="sxs-lookup"><span data-stu-id="76995-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-171">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="76995-172">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="76995-173">IotHub sistem ve cihaz iletilerini işleyebilen yalnızca bir yerleşik uç noktayla ("events") geldiğinden `EventHubEndPointName` parametresi değiştirilmeden kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-174">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="76995-175">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="76995-176">IotHub sistem ve cihaz iletilerini işleyebilen yalnızca bir yerleşik uç noktayla ("events") geldiğinden `EventHubEndPointName` parametresi değiştirilmeden kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-177">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="76995-178">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="76995-179">IotHub sistem ve cihaz iletilerini işleyebilen yalnızca bir yerleşik uç noktayla ("events") geldiğinden `EventHubEndPointName` parametresi değiştirilmeden kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-180">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="76995-181">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="76995-182">IotHub artık yerleşik uç nokta ("operationsMonitoringEvents") kullanmadığından `OperationsMonitoringProperties` parametresi değiştirilmeden kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="76995-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76995-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="76995-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` ve `ASRRecoveryPlanGroup.EndGroupActions` çıkıştan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="76995-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` ve `ASRRecoveryPlanGroup.EndGroupActions` çıkıştan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="76995-186">IncludeDiskId parametresi, Azure Site Recovery’de bir yönetilen diske doğrudan yazmayı destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="76995-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-187">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="76995-188">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="76995-189">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="76995-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="76995-190">Az.Batch Modülü ile Önceki Sürüm Uyumsuzluğu</span><span class="sxs-lookup"><span data-stu-id="76995-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="76995-191">‘Az.Resources’ modülü 1.7.1 sürümü, ‘Az.Batch’ modülünün önceki sürümleriyle (sürüm 1.1.2 veya daha önceki sürümler) uyumlu değildir.</span><span class="sxs-lookup"><span data-stu-id="76995-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="76995-192">Bu, ‘Az.Resources’ modülünün 1.7.1 sürümü içeri aktarıldığında ‘Az.Batch’ modülünün 1.1.2 sürümünün içeri aktarılmamasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="76995-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="76995-193">Bu sorunu düzeltmek için, ‘Az.Batch’ modülünü sürüm 2.0.1 veya sonraki bir sürüme güncelleştirin veya ‘Az’ modülünün en son sürümünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="76995-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="76995-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76995-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="76995-195">Bu senaryo `Add-AzVmssSecret` kapsamında olduğu için `Add-ServiceFabricApplicationCertificate` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-196">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="76995-197">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="76995-198">Sql</span><span class="sxs-lookup"><span data-stu-id="76995-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="76995-199">Güvenli bağlantının kullanım dışı bırakıldığına ve bu nedenle komutun kaldırıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="76995-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="76995-200">Bağlantı dizelerini görüntülemek için lütfen Azure portal SQL veritabanı dikey penceresini kullanın</span><span class="sxs-lookup"><span data-stu-id="76995-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="76995-201">`Get-AzSqlDatabaseIndexRecommendations` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="76995-202">Bunun yerine `Get-AzSqlDatabaseIndexRecommendation` kullanın.</span><span class="sxs-lookup"><span data-stu-id="76995-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="76995-203">`Get-AzSqlDatabaseRestorePoints` diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="76995-204">Bunun yerine `Get-AzSqlDatabaseRestorePoint` kullanın.</span><span class="sxs-lookup"><span data-stu-id="76995-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="76995-205">`Get-AzSqlDatabaseAudit` cmdlet’i bu cmdlet’in yerini alır.</span><span class="sxs-lookup"><span data-stu-id="76995-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="76995-206">Çıkış türü, mevcut 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' türünden yeni 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel' türüne değiştirilerek `AuditState` ve `StorageAccountName` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="76995-207">ve `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="76995-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="76995-208">Betikler, yeni `StorageAccountResourceId` özelliğinden depolama hesabı bilgilerini alabilir.</span><span class="sxs-lookup"><span data-stu-id="76995-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-209">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="76995-210">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="76995-211">`Set-AzSqlDatabaseAudit` cmdlet’i bu cmdlet’in yerini alır.</span><span class="sxs-lookup"><span data-stu-id="76995-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="76995-212">Çıkış türü, mevcut 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' türünden yeni 'bool' türüne değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="76995-213">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-214">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="76995-215">`Get-AzSqlServerAudit` cmdlet’i bu cmdlet’in yerini alır.</span><span class="sxs-lookup"><span data-stu-id="76995-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="76995-216">Çıkış türü, mevcut 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' türünden yeni 'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel' türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="76995-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="76995-217">`AuditState`, `StorageAccountName` ve `StorageAccountSubscriptionId` özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="76995-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="76995-218">`StorageAccountName` ve `StorageAccountSubscriptionId` özelliklerini kullanan betikler, bu bilgileri yeni `StorageAccountResourceId` özelliğinden alabilir.</span><span class="sxs-lookup"><span data-stu-id="76995-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="76995-219">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="76995-220">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="76995-221">`Set-AzSqlServerAudit` cmdlet’i bu cmdlet’in yerini alır.</span><span class="sxs-lookup"><span data-stu-id="76995-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="76995-222">Çıkış türü, mevcut 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' türünden yeni 'bool' türüne değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="76995-223">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="76995-224">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="76995-225">`Get-AzSqlServerAdvancedThreatProtectionSettings` cmdlet’i `Get-AzSqlServerAdvancedThreatProtectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-226">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="76995-227">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="76995-228">`Clear-AzSqlServerAdvancedThreatProtectionSettings` cmdlet’i `Clear-AzSqlServerAdvancedThreatProtectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-229">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="76995-230">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="76995-231">`Update-AzSqlServerAdvancedThreatProtectionSettings` cmdlet’i `Update-AzSqlServerAdvancedThreatProtectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-232">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="76995-233">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="76995-234">`Get-AzSqlDatabaseAdvancedThreatProtectionSettings` cmdlet’i `Get-AzSqlDatabaseAdvancedThreatProtectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-235">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-236">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="76995-237">`Update-AzSqlDatabaseAdvancedThreatProtectionSettings` cmdlet’i `Update-AzSqlDatabaseAdvancedThreatProtectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-238">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="76995-239">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="76995-240">`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` cmdlet’i `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-241">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-242">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-243">`Update-AzSqlDatabaseVulnerabilityAssessmentSettings` cmdlet’i `Update-AzSqlDatabaseVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-244">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="76995-245">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-246">`Get-AzSqlDatabaseVulnerabilityAssessmentSettings` cmdlet’i `Get-AzSqlDatabaseVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-247">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-248">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-249">`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` cmdlet’i `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-250">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-251">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-252">`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` cmdlet’i `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-253">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="76995-254">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-255">`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` cmdlet’i `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-256">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-257">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-258">`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` cmdlet’i `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-259">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-260">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-261">`Update-AzSqlInstanceVulnerabilityAssessmentSettings` cmdlet’i `Update-AzSqlInstanceVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-262">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="76995-263">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-264">`Get-AzSqlInstanceVulnerabilityAssessmentSettings` cmdlet’i `Get-AzSqlInstanceVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-265">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-266">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-267">`Clear-AzSqlInstanceVulnerabilityAssessmentSettings` cmdlet’i `Clear-AzSqlInstanceVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-268">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-269">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-270">`Update-AzSqlServerVulnerabilityAssessmentSettings` cmdlet’i `Update-AzSqlServerVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-271">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="76995-272">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-273">`Get-AzSqlServerVulnerabilityAssessmentSettings` cmdlet’i `Get-AzSqlServerVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-274">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-275">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="76995-276">`Clear-AzSqlServerVulnerabilityAssessmentSettings` cmdlet’i `Clear-AzSqlServerVulnerabilityAssessmentSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-277">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-278">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="76995-279">`Get-AzSqlServerAdvancedThreatProtectionPolicy` cmdlet’i silindi ve hiçbir cmdlet ile değiştirilmedi</span><span class="sxs-lookup"><span data-stu-id="76995-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="76995-280">`Get-AzSqlServerThreatDetectionPolicy` cmdlet’i `Get-AzSqlServerThreatDetectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-281">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="76995-282">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="76995-283">`Remove-AzSqlServerThreatDetectionPolicy` cmdlet’i `Clear-AzSqlServerThreatDetectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-284">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="76995-285">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="76995-286">`Set-AzSqlServerThreatDetectionPolicy` cmdlet’i `Update-AzSqlServerThreatDetectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-287">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="76995-288">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="76995-289">`Get-AzSqlDatabaseThreatDetectionPolicy` cmdlet’i `Get-AzSqlDatabaseThreatDetectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-290">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="76995-291">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="76995-292">`Set-AzSqlDatabaseThreatDetectionPolicy` cmdlet’i `Update-AzSqlDatabaseThreatDetectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-293">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="76995-294">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="76995-295">`Remove-AzSqlDatabaseThreatDetectionPolicy` cmdlet’i `Clear-AzSqlDatabaseThreatDetectionSetting` ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="76995-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="76995-296">Önce</span><span class="sxs-lookup"><span data-stu-id="76995-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="76995-297">Sonra</span><span class="sxs-lookup"><span data-stu-id="76995-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
