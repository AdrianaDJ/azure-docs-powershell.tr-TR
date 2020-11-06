---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bf049e18d75867f7dd9904e8d2ab2223dffdb0bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573337"
---
# <span data-ttu-id="8d2af-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8d2af-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="8d2af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d2af-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2af-103">Azure Site Recovery çoğaltma ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d2af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d2af-104">SYNTAX</span></span>

### <span data-ttu-id="8d2af-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d2af-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2af-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8d2af-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2af-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8d2af-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d2af-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8d2af-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2af-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8d2af-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2af-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8d2af-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d2af-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d2af-111">DESCRIPTION</span></span>
<span data-ttu-id="8d2af-112">**Update-AzureRmRecoveryServicesAsrPolicy** cmdlet 'ı belirtilen Azure Site Recovery çoğaltma ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="8d2af-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d2af-113">EXAMPLES</span></span>

### <span data-ttu-id="8d2af-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8d2af-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="8d2af-115">Belirtilen parametreleri kullanarak çoğaltmayı Güncelleştir ilkesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8d2af-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8d2af-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8d2af-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="8d2af-117">Belirtilen parametreleri kullanarak Azure 'dan Azure çoğaltma ilkesini Güncelleştir işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8d2af-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8d2af-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8d2af-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="8d2af-119">Azure 'dan Azure çoğaltma ilkesini belirtilen parametreleri kullanarak başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8d2af-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8d2af-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d2af-120">PARAMETERS</span></span>

### <span data-ttu-id="8d2af-121">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="8d2af-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="8d2af-122">Uygulamayla tutarlı kurtarma noktalarının oluşturulacağı sıklığı (saat) belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-123">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="8d2af-123">-Authentication</span></span>
<span data-ttu-id="8d2af-124">Kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-124">Specifies the type of authentication used.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8d2af-125">-AzureToAzure</span></span>
<span data-ttu-id="8d2af-126">İki Azure bölgesi arasında Azure sanal makinelerini çoğaltmak için kullanılan çoğaltma ilkesinin güncelleştirileceğini belirten Switch parametresi güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8d2af-127">-AzureToVMware</span></span>
<span data-ttu-id="8d2af-128">Azure 'da çalışan sanal makinelerin başarısız olduğunu bir şirket içi VMware sitesine geri döndürmek için, belirtilen ilkenin kullanıldığını belirten değer parametresi.</span><span class="sxs-lookup"><span data-stu-id="8d2af-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-129">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="8d2af-129">-Compression</span></span>
<span data-ttu-id="8d2af-130">Sıkıştırmanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8d2af-131">-Confirm</span></span>
<span data-ttu-id="8d2af-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d2af-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2af-133">-DefaultProfile</span></span>
<span data-ttu-id="8d2af-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d2af-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-135">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="8d2af-135">-Encryption</span></span>
<span data-ttu-id="8d2af-136">Şifrelemenin etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-136">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8d2af-137">-HyperVToAzure</span></span>
<span data-ttu-id="8d2af-138">Hyper-V sanal makinelerinin Azure 'a çoğaltılması için belirtilen ilkenin kullanıldığını belirten Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="8d2af-138">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d2af-139">-InputObject</span></span>
<span data-ttu-id="8d2af-140">Cmdlet için giriş nesnesi: güncelleştirilecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-140">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="8d2af-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="8d2af-142">İlke için çoklu VM eşitleme durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-143">-Numberofrecoverypointstokoru</span><span class="sxs-lookup"><span data-stu-id="8d2af-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="8d2af-144">Korunacak sayı kurtarma noktalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-145">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="8d2af-145">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="8d2af-146">, Uyarmak için dakika cinsinden RPO eşik değeri.</span><span class="sxs-lookup"><span data-stu-id="8d2af-146">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-147">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="8d2af-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8d2af-148">Çoğaltma hedefinin Azure depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-148">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="8d2af-149">New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet kullanılarak çoğaltmayı etkinleştirirken alternatif sağlanmadıysa, çoğaltma için hedef depolama hesabı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8d2af-149">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-150">-Recoverypointretentionınhours</span><span class="sxs-lookup"><span data-stu-id="8d2af-150">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="8d2af-151">Oluşturulduktan sonra kurtarma noktalarını korumak için saat cinsinden süre.</span><span class="sxs-lookup"><span data-stu-id="8d2af-151">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-152">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="8d2af-152">-ReplicaDeletion</span></span>
<span data-ttu-id="8d2af-153">VMM yönetilen sitesinden diğerine çoğaltma devre dışı bırakılırken çoğaltma sanal makinesinin silinip silinmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-153">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-154">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="8d2af-154">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="8d2af-155">Çoğaltma sıklığı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-155">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="8d2af-156">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8d2af-156">Valid values are:</span></span>

- <span data-ttu-id="8d2af-157">30</span><span class="sxs-lookup"><span data-stu-id="8d2af-157">30</span></span>
- <span data-ttu-id="8d2af-158">300</span><span class="sxs-lookup"><span data-stu-id="8d2af-158">300</span></span>
- <span data-ttu-id="8d2af-159">900</span><span class="sxs-lookup"><span data-stu-id="8d2af-159">900</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-160">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="8d2af-160">-ReplicationMethod</span></span>
<span data-ttu-id="8d2af-161">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-161">Specifies the replication method.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="8d2af-162">-ReplicationPort</span></span>
<span data-ttu-id="8d2af-163">Çoğaltma için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-163">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-164">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="8d2af-164">-ReplicationStartTime</span></span>
<span data-ttu-id="8d2af-165">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-165">Specifies the replication start time.</span></span>
<span data-ttu-id="8d2af-166">İşin başında 24 saatten sonra olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-166">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8d2af-167">-VMwareToAzure</span></span>
<span data-ttu-id="8d2af-168">VMware sanal makinelerini Azure 'a çoğaltmak için belirtilen ilkenin kullanıldığını belirten Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="8d2af-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="8d2af-169">-VmmToVmm</span></span>
<span data-ttu-id="8d2af-170">İki Hyper-V sitesi arasında VMM yönetilen Hyper-V sanal makinelerini çoğaltmak için belirtilen ilkenin kullanıldığını belirten Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="8d2af-170">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d2af-171">-WhatIf</span></span>
<span data-ttu-id="8d2af-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d2af-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d2af-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8d2af-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2af-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2af-174">CommonParameters</span></span>
<span data-ttu-id="8d2af-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d2af-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2af-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d2af-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2af-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d2af-177">INPUTS</span></span>

### <span data-ttu-id="8d2af-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="8d2af-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="8d2af-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d2af-179">OUTPUTS</span></span>

### <span data-ttu-id="8d2af-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="8d2af-180">System.Object</span></span>

## <span data-ttu-id="8d2af-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d2af-181">NOTES</span></span>

## <span data-ttu-id="8d2af-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d2af-182">RELATED LINKS</span></span>
