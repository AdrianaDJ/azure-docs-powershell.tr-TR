---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274246"
---
# <span data-ttu-id="2d2ac-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2d2ac-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="2d2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2ac-103">Azure Site Recovery çoğaltma ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="2d2ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d2ac-104">SYNTAX</span></span>

### <span data-ttu-id="2d2ac-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d2ac-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d2ac-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2d2ac-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d2ac-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2d2ac-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d2ac-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="2d2ac-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d2ac-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="2d2ac-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d2ac-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="2d2ac-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d2ac-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d2ac-111">DESCRIPTION</span></span>
<span data-ttu-id="2d2ac-112">**Update-AzRecoveryServicesAsrPolicy** cmdlet 'i, belirtilen Azure Site Recovery çoğaltma ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="2d2ac-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d2ac-113">EXAMPLES</span></span>

### <span data-ttu-id="2d2ac-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d2ac-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="2d2ac-115">Belirtilen parametreleri kullanarak çoğaltmayı Güncelleştir ilkesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2d2ac-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2d2ac-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="2d2ac-117">Belirtilen parametreleri kullanarak Azure 'dan Azure çoğaltma ilkesini Güncelleştir işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2d2ac-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2d2ac-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="2d2ac-119">Azure 'dan Azure çoğaltma ilkesini belirtilen parametreleri kullanarak başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2d2ac-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d2ac-120">PARAMETERS</span></span>

### <span data-ttu-id="2d2ac-121">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="2d2ac-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="2d2ac-122">Uygulamayla tutarlı kurtarma noktalarının oluşturulacağı sıklığı (saat) belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-123">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="2d2ac-123">-Authentication</span></span>
<span data-ttu-id="2d2ac-124">Kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2d2ac-125">-AzureToAzure</span></span>
<span data-ttu-id="2d2ac-126">Azure 'dan Azure olağanüstü durum kurtarması 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-126">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="2d2ac-127">-AzureToVMware</span></span>
<span data-ttu-id="2d2ac-128">Azure to vMWare olağanüstü durum kurtarması 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-128">Specifies the Azure to vMWare disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-129">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="2d2ac-129">-Compression</span></span>
<span data-ttu-id="2d2ac-130">Sıkıştırmanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2ac-131">-DefaultProfile</span></span>
<span data-ttu-id="2d2ac-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="2d2ac-133">-HyperVToAzure</span></span>
<span data-ttu-id="2d2ac-134">Hyper-V sanal makinelerinin Azure 'a çoğaltılması için belirtilen ilkenin kullanıldığını belirten Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d2ac-135">-InputObject</span></span>
<span data-ttu-id="2d2ac-136">Cmdlet için giriş nesnesi: güncelleştirilecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="2d2ac-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="2d2ac-138">İlke için çoklu VM eşitleme durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-139">-Numberofrecoverypointstokoru</span><span class="sxs-lookup"><span data-stu-id="2d2ac-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="2d2ac-140">Korunacak sayı kurtarma noktalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-141">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="2d2ac-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="2d2ac-142">Çoğaltma hedefinin Azure depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="2d2ac-143">New-AzRecoveryServicesASRReplicationProtectedItem cmdlet kullanılarak çoğaltmayı etkinleştirirken alternatif sağlanmadıysa, çoğaltma için hedef depolama hesabı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-144">-Recoverypointretentionınhours</span><span class="sxs-lookup"><span data-stu-id="2d2ac-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="2d2ac-145">Oluşturulduktan sonra kurtarma noktalarını korumak için saat cinsinden süre.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-146">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="2d2ac-146">-ReplicaDeletion</span></span>
<span data-ttu-id="2d2ac-147">VMM yönetilen sitesinden diğerine çoğaltma devre dışı bırakılırken çoğaltma sanal makinesinin silinip silinmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="2d2ac-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="2d2ac-149">Çoğaltma sıklığı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="2d2ac-150">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="2d2ac-150">Valid values are:</span></span>

- <span data-ttu-id="2d2ac-151">30</span><span class="sxs-lookup"><span data-stu-id="2d2ac-151">30</span></span>
- <span data-ttu-id="2d2ac-152">300</span><span class="sxs-lookup"><span data-stu-id="2d2ac-152">300</span></span>
- <span data-ttu-id="2d2ac-153">900</span><span class="sxs-lookup"><span data-stu-id="2d2ac-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="2d2ac-154">-ReplicationMethod</span></span>
<span data-ttu-id="2d2ac-155">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="2d2ac-156">-ReplicationPort</span></span>
<span data-ttu-id="2d2ac-157">Çoğaltma için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="2d2ac-158">-ReplicationStartTime</span></span>
<span data-ttu-id="2d2ac-159">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-159">Specifies the replication start time.</span></span>
<span data-ttu-id="2d2ac-160">İşin başında 24 saatten sonra olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="2d2ac-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="2d2ac-162">, Uyarmak için dakika cinsinden RPO eşik değeri.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="2d2ac-163">-VmmToVmm</span></span>
<span data-ttu-id="2d2ac-164">İki Hyper-V sitesi arasında VMM yönetilen Hyper-V sanal makinelerini yinelemek için belirtilen ilkenin kullanıldığını belirten Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2d2ac-165">-VMwareToAzure</span></span>
<span data-ttu-id="2d2ac-166">VMware sanal makinelerini Azure 'a çoğaltmak için belirtilen ilkenin kullanıldığını belirten Switch parametresi.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d2ac-167">-Confirm</span></span>
<span data-ttu-id="2d2ac-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2ac-169">-WhatIf</span></span>
<span data-ttu-id="2d2ac-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d2ac-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2ac-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2ac-172">CommonParameters</span></span>
<span data-ttu-id="2d2ac-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2ac-174">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2d2ac-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2ac-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d2ac-175">INPUTS</span></span>

### <span data-ttu-id="2d2ac-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="2d2ac-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="2d2ac-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d2ac-177">OUTPUTS</span></span>

### <span data-ttu-id="2d2ac-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2d2ac-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2d2ac-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d2ac-179">NOTES</span></span>

## <span data-ttu-id="2d2ac-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d2ac-180">RELATED LINKS</span></span>
