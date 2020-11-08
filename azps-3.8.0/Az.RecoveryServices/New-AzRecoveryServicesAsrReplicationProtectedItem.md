---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3d9cd1bface4175e60b45d6865815f1a4ea964f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098166"
---
# <span data-ttu-id="faf88-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="faf88-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="faf88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf88-102">SYNOPSIS</span></span>
<span data-ttu-id="faf88-103">Çoğaltma korumalı bir öğe oluşturarak, bir ASR korunabilir öğesi için çoğaltmayı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="faf88-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="faf88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="faf88-104">SYNTAX</span></span>

### <span data-ttu-id="faf88-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="faf88-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf88-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="faf88-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf88-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="faf88-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf88-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="faf88-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf88-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="faf88-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf88-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="faf88-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf88-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="faf88-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf88-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="faf88-112">DESCRIPTION</span></span>
<span data-ttu-id="faf88-113">**Yeni-Azrecoveryservicesasrreplicationkorutdıtem** cmdlet 'i, yeni bir çoğaltma korumalı öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="faf88-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="faf88-114">ASR korunabilir öğesi için yinelemeyi etkinleştirmek üzere bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="faf88-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="faf88-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="faf88-115">EXAMPLES</span></span>

### <span data-ttu-id="faf88-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="faf88-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="faf88-117">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="faf88-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="faf88-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="faf88-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="faf88-119">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure senaryosuna) döndürür.</span><span class="sxs-lookup"><span data-stu-id="faf88-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="faf88-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="faf88-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="faf88-121">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="faf88-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="faf88-122">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="faf88-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="faf88-123">Belirtilen VMID için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="faf88-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="faf88-124">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="faf88-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="faf88-125">Seçmeli diskler dahil olmak üzere belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve seçili disklerle işlemi izlemek için kullanılan ASR işini (vmWare-Azure senaryosu) döndürür.</span><span class="sxs-lookup"><span data-stu-id="faf88-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="faf88-126">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="faf88-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="faf88-127">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="faf88-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="faf88-128">Belirtilen VMID için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure 'a) döndürür. Şifreleme cmdlet 'inde geçirilen yük devretme VM ayrıntıları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="faf88-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

## <span data-ttu-id="faf88-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="faf88-129">PARAMETERS</span></span>

### <span data-ttu-id="faf88-130">-Hesap</span><span class="sxs-lookup"><span data-stu-id="faf88-130">-Account</span></span>
<span data-ttu-id="faf88-131">Gerekirse Mobility hizmetini göndermek için kullanılacak farklı hesapla hesabı.</span><span class="sxs-lookup"><span data-stu-id="faf88-131">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="faf88-132">ASR yapısı 'nda farklı Run as hesapları listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="faf88-132">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-133">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="faf88-133">-AzureToAzure</span></span>
<span data-ttu-id="faf88-134">Switch parametresi Azure 'dan Azure 'da yinelenen öğenin oluşturulmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-134">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-135">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf88-135">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="faf88-136">Azure için VM 'den Azure olağanüstü durum kurtarma senaryosuna kullanılacak disk yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-136">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-137">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="faf88-137">-AzureVmId</span></span>
<span data-ttu-id="faf88-138">Kurtarma bölgesindeki olağanüstü durum kurtarma koruması için Azure VM kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-138">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf88-139">-DefaultProfile</span></span>
<span data-ttu-id="faf88-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="faf88-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="faf88-141">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="faf88-141">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="faf88-142">Yük devretme sonrasında kurtarma VM olarak kullanılacak sürüm (Azure disk şifrelemesi) içeren disk şifrelemesi gizlilik URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-142">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-143">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="faf88-143">-DiskEncryptionSetId</span></span>
<span data-ttu-id="faf88-144">Yönetilen disklerin şifrelenmesi için kullanılacak disk şifrelemesi kümesinin kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-144">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-145">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="faf88-145">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="faf88-146">Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi gizli kasası KIMLIĞINI (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-146">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-147">-DiskType</span><span class="sxs-lookup"><span data-stu-id="faf88-147">-DiskType</span></span>
<span data-ttu-id="faf88-148">Kurtarma VM yönetimli disk türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-148">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="faf88-149">-HyperVToAzure</span></span>
<span data-ttu-id="faf88-150">Azure 'a çoğaltılan bir Hyper-V sanal makinesi çoğaltılmış öğenin belirtilmesi için anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="faf88-150">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-151">-Includediskid</span><span class="sxs-lookup"><span data-stu-id="faf88-151">-IncludeDiskId</span></span>
<span data-ttu-id="faf88-152">Çoğaltmaya eklenecek disklerin listesi.</span><span class="sxs-lookup"><span data-stu-id="faf88-152">The list of disks to include for replication.</span></span> <span data-ttu-id="faf88-153">Varsayılan olarak tüm diskler dahildir.</span><span class="sxs-lookup"><span data-stu-id="faf88-153">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-154">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="faf88-154">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="faf88-155">Belirtilen korunabilir öğeden korunacak vMWare disk kimliği için disk yapılandırması girişini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-155">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-156">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="faf88-156">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="faf88-157">Sürüm yerine çalışma sonrasında kurtarma VM olarak kullanılacak sürüm (Azure disk şifrelemesi) içeren disk şifrelemesi anahtar URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-157">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-158">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="faf88-158">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="faf88-159">Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi anahtarı Anahtar Kasası KIMLIĞI 'ni (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-159">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-160">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="faf88-160">-LogStorageAccountId</span></span>
<span data-ttu-id="faf88-161">Çoğaltma günlüklerinin depolanacağı günlük veya önbellek hesap kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-161">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-162">-Ad</span><span class="sxs-lookup"><span data-stu-id="faf88-162">-Name</span></span>
<span data-ttu-id="faf88-163">ASR çoğaltması korumalı öğesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-163">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="faf88-164">Adın kasa içinde benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="faf88-164">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="faf88-165">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="faf88-165">-OS</span></span>
<span data-ttu-id="faf88-166">İşletim sistemi ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-166">Specifies the operating system family.</span></span>
<span data-ttu-id="faf88-167">Bu parametre için kabul edilebilir değerler: Windows veya Linux.</span><span class="sxs-lookup"><span data-stu-id="faf88-167">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-168">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="faf88-168">-OSDiskName</span></span>
<span data-ttu-id="faf88-169">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-169">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-170">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="faf88-170">-ProcessServer</span></span>
<span data-ttu-id="faf88-171">Bu makineyi çoğaltmak için kullanılacak Işlem sunucusu.</span><span class="sxs-lookup"><span data-stu-id="faf88-171">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="faf88-172">Yapılandırma sunucusuna karşılık gelen ASR yapısı içinde bir tane belirtmek için, sunucu listesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="faf88-172">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-173">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="faf88-173">-ProtectableItem</span></span>
<span data-ttu-id="faf88-174">Çoğaltmanın etkinleştirildiği ASR korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-174">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-175">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="faf88-175">-ProtectionContainerMapping</span></span>
<span data-ttu-id="faf88-176">Çoğaltma için kullanılacak çoğaltma ilkesine karşılık gelen ASR koruma kapsayıcısı eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-176">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-177">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="faf88-177">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="faf88-178">Makineyi yük devretmenin olayında kurtarmak için kullanılabilirlik kümesi KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="faf88-178">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-179">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="faf88-179">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="faf88-180">Yük devretmenin ardından kurtarma VM kullanılabilirlik bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-180">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-181">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="faf88-181">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="faf88-182">Başarısızlık durumunda makineyi kurtarmak için Azure sanal ağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="faf88-182">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-183">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="faf88-183">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="faf88-184">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-184">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-185">-Kurtarılan ağ adı</span><span class="sxs-lookup"><span data-stu-id="faf88-185">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="faf88-186">Yük devretme olayında sanal makinenin yük devretmekte olduğu, kurtarma Azure sanal ağındaki alt ağ.</span><span class="sxs-lookup"><span data-stu-id="faf88-186">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-187">-Recoverybootdiagstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="faf88-187">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="faf88-188">Kurtarma Azure VM için önyükleme tanılaması depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-188">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-189">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="faf88-189">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="faf88-190">Bu sanal makinenin yük devretmesi için kurtarma bulut hizmetinin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-190">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-191">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="faf88-191">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="faf88-192">Yük devretme olayında sanal makinenin oluşturulduğu kaynak grubunun ARM tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-192">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-193">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="faf88-193">-RecoveryVmName</span></span>
<span data-ttu-id="faf88-194">Yük devretme sonrasında oluşturulan kurtarma VM 'sinin adı.</span><span class="sxs-lookup"><span data-stu-id="faf88-194">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-195">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="faf88-195">-ReplicationGroupName</span></span>
<span data-ttu-id="faf88-196">Çoklu VM tutarlı kurtarma noktaları oluşturmak için kullanılacak çoğaltma grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-196">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="faf88-197">Varsayılan olarak, her çoğaltma korumalı öğesi kendi bir grubunda oluşturulur ve çoklu VM uyumlu kurtarma noktaları oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="faf88-197">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="faf88-198">Tüm makineleri aynı çoğaltma grubuna koruyarak, bir makine grubu genelinde çok sunuculu tutarlı kurtarma noktaları oluşturmanız gerekiyorsa bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="faf88-198">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-199">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="faf88-199">-VmmToVmm</span></span>
<span data-ttu-id="faf88-200">Yinelenen öğenin, VMM yönetilen Hyper-V siteleri arasında çoğaltılmış bir Hyper-V sanal makinesi olduğunu belirtmek için anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="faf88-200">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="faf88-201">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="faf88-201">-VMwareToAzure</span></span>
<span data-ttu-id="faf88-202">Azure 'a çoğaltılacak olan bir VMware sanal makinesi ya da fiziksel sunucusu, çoğaltılmış öğeyi belirtecek şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="faf88-202">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-203">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="faf88-203">-WaitForCompletion</span></span>
<span data-ttu-id="faf88-204">Cmdlet 'in işlemin tamamlanması için beklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf88-204">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf88-205">-Onay</span><span class="sxs-lookup"><span data-stu-id="faf88-205">-Confirm</span></span>
<span data-ttu-id="faf88-206">İşlemi başlatmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="faf88-206">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="faf88-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf88-207">-WhatIf</span></span>
<span data-ttu-id="faf88-208">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="faf88-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faf88-209">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="faf88-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf88-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf88-210">CommonParameters</span></span>
<span data-ttu-id="faf88-211">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="faf88-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf88-212">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="faf88-212">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf88-213">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="faf88-213">INPUTS</span></span>

### <span data-ttu-id="faf88-214">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="faf88-214">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="faf88-215">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="faf88-215">OUTPUTS</span></span>

### <span data-ttu-id="faf88-216">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="faf88-216">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="faf88-217">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="faf88-217">NOTES</span></span>

## <span data-ttu-id="faf88-218">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="faf88-218">RELATED LINKS</span></span>

[<span data-ttu-id="faf88-219">Get-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="faf88-219">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="faf88-220">Remove-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="faf88-220">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="faf88-221">Set-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="faf88-221">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
