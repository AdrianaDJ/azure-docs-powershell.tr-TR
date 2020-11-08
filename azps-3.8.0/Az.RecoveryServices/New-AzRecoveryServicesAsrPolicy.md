---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104701"
---
# <span data-ttu-id="3eeab-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="3eeab-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="3eeab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eeab-102">SYNOPSIS</span></span>
<span data-ttu-id="3eeab-103">Azure Site Recovery çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3eeab-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="3eeab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3eeab-104">SYNTAX</span></span>

### <span data-ttu-id="3eeab-105">Hipervtoazure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3eeab-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eeab-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="3eeab-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eeab-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="3eeab-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eeab-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3eeab-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eeab-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="3eeab-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eeab-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="3eeab-110">DESCRIPTION</span></span>
<span data-ttu-id="3eeab-111">**New-AzRecoveryServicesAsrPolicy** cmdlet 'ı Azure Site Recovery çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3eeab-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="3eeab-112">Çoğaltma İlkesi, çoğaltma sıklığı ve kurtarma noktaları sayısı gibi çoğaltma ayarlarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3eeab-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="3eeab-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3eeab-113">EXAMPLES</span></span>

### <span data-ttu-id="3eeab-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3eeab-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="3eeab-115">Belirtilen parametreleri kullanarak çoğaltma ilkesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3eeab-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="3eeab-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3eeab-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="3eeab-117">Belirtilen parametreleri kullanarak çoğaltma ilkesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3eeab-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="3eeab-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3eeab-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="3eeab-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="3eeab-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="3eeab-120">Belirtilen parametreleri kullanarak çoğaltma ilkesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3eeab-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3eeab-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3eeab-121">PARAMETERS</span></span>

### <span data-ttu-id="3eeab-122">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="3eeab-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="3eeab-123">Uygulamayla tutarlı kurtarma noktalarının oluşturulacağı sıklığı (saat) belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="3eeab-124">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="3eeab-124">-Authentication</span></span>
<span data-ttu-id="3eeab-125">Kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="3eeab-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3eeab-126">Valid values are:</span></span>

- <span data-ttu-id="3eeab-127">Sertifika</span><span class="sxs-lookup"><span data-stu-id="3eeab-127">Certificate</span></span>
-  <span data-ttu-id="3eeab-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="3eeab-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3eeab-129">-AzureToAzure</span></span>
<span data-ttu-id="3eeab-130">Switch parametresi Azure için Azure ilke oluşturma senaryosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="3eeab-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="3eeab-131">-AzureToVMware</span></span>
<span data-ttu-id="3eeab-132">Switch parametresi Azure 'dan vMWare ilke oluşturma senaryosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="3eeab-133">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="3eeab-133">-Compression</span></span>
<span data-ttu-id="3eeab-134">Sıkıştırmanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eeab-135">-DefaultProfile</span></span>
<span data-ttu-id="3eeab-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3eeab-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3eeab-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="3eeab-137">-HyperVToAzure</span></span>
<span data-ttu-id="3eeab-138">Hyper-V sanal makinelerinin Azure 'a çoğaltılması</span><span class="sxs-lookup"><span data-stu-id="3eeab-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="3eeab-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="3eeab-140">İlke için çoklu VM eşitleme durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="3eeab-141">-Name</span></span>
<span data-ttu-id="3eeab-142">ASR çoğaltma ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-142">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-143">-Numberofrecoverypointstokoru</span><span class="sxs-lookup"><span data-stu-id="3eeab-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="3eeab-144">Korunacak sayı kurtarma noktalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-145">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="3eeab-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="3eeab-146">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-147">-Recoverypointretentionınhours</span><span class="sxs-lookup"><span data-stu-id="3eeab-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="3eeab-148">Verilen zaman için kurtarma noktalarını saat cinsinden tutma.</span><span class="sxs-lookup"><span data-stu-id="3eeab-148">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-149">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="3eeab-149">-ReplicaDeletion</span></span>
<span data-ttu-id="3eeab-150">VMM yönetilen sitesinden diğerine çoğaltma devre dışı bırakılırken çoğaltma sanal makinesinin silinip silinmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="3eeab-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="3eeab-152">Çoğaltma sıklığı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="3eeab-153">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3eeab-153">Valid values are:</span></span>

- <span data-ttu-id="3eeab-154">30</span><span class="sxs-lookup"><span data-stu-id="3eeab-154">30</span></span>
- <span data-ttu-id="3eeab-155">300</span><span class="sxs-lookup"><span data-stu-id="3eeab-155">300</span></span>
- <span data-ttu-id="3eeab-156">900</span><span class="sxs-lookup"><span data-stu-id="3eeab-156">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="3eeab-157">-ReplicationMethod</span></span>
<span data-ttu-id="3eeab-158">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-158">Specifies the replication method.</span></span>
<span data-ttu-id="3eeab-159">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3eeab-159">Valid values are:</span></span>

- <span data-ttu-id="3eeab-160">Medya</span><span class="sxs-lookup"><span data-stu-id="3eeab-160">Online</span></span>
- <span data-ttu-id="3eeab-161">Çalış</span><span class="sxs-lookup"><span data-stu-id="3eeab-161">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="3eeab-162">-ReplicationPort</span></span>
<span data-ttu-id="3eeab-163">Çoğaltma için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-163">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="3eeab-164">-ReplicationProvider</span></span>
<span data-ttu-id="3eeab-165">İlkenin çoğaltma sağlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-165">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="3eeab-166">-ReplicationStartTime</span></span>
<span data-ttu-id="3eeab-167">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-167">Specifies the replication start time.</span></span>
<span data-ttu-id="3eeab-168">İşin başında 24 saatten sonra olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-168">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="3eeab-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="3eeab-170">, Uyarmak için dakika cinsinden RPO eşik değeri.</span><span class="sxs-lookup"><span data-stu-id="3eeab-170">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="3eeab-171">-VmmToVmm</span></span>
<span data-ttu-id="3eeab-172">Bir VMM sunucusu tarafından yönetilen Hyper-V siteleri arasında çoğaltma için ilkeyi belirtecek şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="3eeab-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eeab-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="3eeab-173">-VMwareToAzure</span></span>
<span data-ttu-id="3eeab-174">Oluşturulan çoğaltma ilkesinin VMware sanal makinelerini ve/veya fiziksel sunucularını Azure 'a çoğaltmak için kullanılacağını belirten geçiş parametresi.</span><span class="sxs-lookup"><span data-stu-id="3eeab-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="3eeab-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="3eeab-175">-Confirm</span></span>
<span data-ttu-id="3eeab-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3eeab-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eeab-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eeab-177">-WhatIf</span></span>
<span data-ttu-id="3eeab-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3eeab-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3eeab-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3eeab-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eeab-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eeab-180">CommonParameters</span></span>
<span data-ttu-id="3eeab-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3eeab-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eeab-182">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3eeab-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eeab-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3eeab-183">INPUTS</span></span>

### <span data-ttu-id="3eeab-184">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3eeab-184">None</span></span>

## <span data-ttu-id="3eeab-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3eeab-185">OUTPUTS</span></span>

### <span data-ttu-id="3eeab-186">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3eeab-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3eeab-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3eeab-187">NOTES</span></span>

## <span data-ttu-id="3eeab-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3eeab-188">RELATED LINKS</span></span>

[<span data-ttu-id="3eeab-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="3eeab-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="3eeab-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="3eeab-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
