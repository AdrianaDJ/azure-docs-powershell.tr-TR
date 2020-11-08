---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279174"
---
# <span data-ttu-id="5bdbb-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="5bdbb-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="5bdbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bdbb-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdbb-103">Belirtilen çoğaltma korumalı öğesi veya kurtarma planı için çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="5bdbb-104">Yinelenen öğeyi veya kurtarma planını geri çevirmek/geri çevirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="5bdbb-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bdbb-105">SYNTAX</span></span>

### <span data-ttu-id="5bdbb-106">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5bdbb-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="5bdbb-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5bdbb-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="5bdbb-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5bdbb-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5bdbb-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5bdbb-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5bdbb-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdbb-114">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="5bdbb-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdbb-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bdbb-115">DESCRIPTION</span></span>
<span data-ttu-id="5bdbb-116">**Update-AzRecoveryServicesAsrProtectionDirection** cmdlet 'i, bir yürütme yük devretmesi işlemi tamamlandıktan sonra belirtilen Azure Site Recovery nesnesinin çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="5bdbb-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bdbb-117">EXAMPLES</span></span>

### <span data-ttu-id="5bdbb-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5bdbb-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="5bdbb-119">Belirtilen kurtarma planı için yön güncelleştirme işlemini başlatın ve işlemi izlemek için kullanılan ASR iş nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="5bdbb-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5bdbb-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="5bdbb-121">Koruma kapsayıcısı eşlemesi ve önbellek depolama alanı (VM ile aynı bölgede) kullanılarak tanımlanan hedef Azure bölgesinde belirtilen çoğaltma korumalı öğesi için güncelleştirme yönü işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="5bdbb-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5bdbb-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="5bdbb-123">Koruma kapsayıcısı eşleme tarafından tanımlanan hedef Azure bölgesinde belirtilen çoğaltma korumalı öğesi için korumayı Güncelleştir işlemini başlatın ve sağlanan disk çoğaltma yapılandırması sağlanır.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="5bdbb-124">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="5bdbb-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="5bdbb-125">Koruma kapsayıcısı eşlemesi ve sağlanan disk çoğaltma yapılandırması tarafından tanımlanan hedef Azure bölgesinde belirtilen şifreli çoğaltma korumalı öğesi için güncelleştirme yönü işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="5bdbb-126">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="5bdbb-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="5bdbb-127">Koruma kapsayıcısı eşlemesi ve önbellek depolama alanı (VM ile aynı bölgede) ile yakınlık yerleştirme grubuyla tanımlanan hedef Azure bölgesinde belirtilen çoğaltma korumalı öğesi için güncelleştirme yönü işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="5bdbb-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bdbb-128">PARAMETERS</span></span>

### <span data-ttu-id="5bdbb-129">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5bdbb-129">-Account</span></span>
<span data-ttu-id="5bdbb-130">Gerekirse Mobility hizmetini göndermek için kullanılacak farklı hesapla hesabı.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="5bdbb-131">ASR yapısı 'nda farklı Run as hesapları listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5bdbb-132">-AzureToAzure</span></span>
<span data-ttu-id="5bdbb-133">Azure 'dan Azure olağanüstü durum kurtarması 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bdbb-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="5bdbb-135">Olağanüstü durum kurtarması için disk yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="5bdbb-136">-AzureToVMware</span></span>
<span data-ttu-id="5bdbb-137">Azure to vMWare senaryosunu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="5bdbb-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="5bdbb-138">-DataStore</span></span>
<span data-ttu-id="5bdbb-139">Vmdisk için kullanılacak VMware veri deposu.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdbb-140">-DefaultProfile</span></span>
<span data-ttu-id="5bdbb-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5bdbb-142">-Yön</span><span class="sxs-lookup"><span data-stu-id="5bdbb-142">-Direction</span></span>
<span data-ttu-id="5bdbb-143">Bir yük devretme sonrası güncelleştirme işleminde kullanılacak yönü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="5bdbb-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5bdbb-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bdbb-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5bdbb-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="5bdbb-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5bdbb-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="5bdbb-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="5bdbb-148">Yük devretme sonrasında kurtarma VM olarak kullanılacak sürüm (Azure disk şifrelemesi) içeren disk şifrelemesi gizlilik URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="5bdbb-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="5bdbb-150">Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi gizli kasası KIMLIĞINI (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="5bdbb-151">-HyperVToAzure</span></span>
<span data-ttu-id="5bdbb-152">Yeniden başlatıldıktan sonra Hyper-V sanal makinesini yeniden koruyun.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="5bdbb-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="5bdbb-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="5bdbb-154">Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi anahtar URL 'sini (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="5bdbb-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="5bdbb-156">Yük devretmenin ardından kurtarma VM olarak kullanılacak Anahtar Kasası KIMLIĞI 'ni (Azure disk şifrelemesi) belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-157">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5bdbb-157">-LogStorageAccountId</span></span>
<span data-ttu-id="5bdbb-158">VM 'lerin çoğaltma günlüğünün depolanacağı depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="5bdbb-159">-MasterTarget</span></span>
<span data-ttu-id="5bdbb-160">Ana hedef sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="5bdbb-161">-ProcessServer</span></span>
<span data-ttu-id="5bdbb-162">Çoğaltma için kullanılacak sunucu.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5bdbb-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="5bdbb-164">Çoğaltma için kullanılacak koruma containerMapping.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5bdbb-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="5bdbb-166">Yük devretmenin ardından sanal makinenin oluşturulması gereken kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="5bdbb-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-167">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5bdbb-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="5bdbb-168">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-169">-Recoverybootdiagstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5bdbb-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="5bdbb-170">Kurtarma Azure VM için önyükleme tanılaması depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-171">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="5bdbb-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="5bdbb-172">Bu sanal makinenin yük devretmesine yönelik kurtarma bulut hizmetinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bdbb-173">-RecoveryPlan</span></span>
<span data-ttu-id="5bdbb-174">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5bdbb-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="5bdbb-176">Bu sanal makinenin yük devretmesi için kurtarma yakınlık yerleştirme grubunun kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-177">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="5bdbb-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="5bdbb-178">Korumalı VM için kurtarma resourceGroup ID.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-179">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="5bdbb-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5bdbb-180">ASR çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="5bdbb-181">-RetentionVolume</span></span>
<span data-ttu-id="5bdbb-182">Ana hedef sunucusundaki bekletme birimi kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdbb-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="5bdbb-183">-VmmToVmm</span></span>
<span data-ttu-id="5bdbb-184">İki VMM yönetimli Hyper-V sitesi arasında korunan Hyper-V sanal makinesinin yük devri için çoğaltma yönünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="5bdbb-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5bdbb-185">-VMwareToAzure</span></span>
<span data-ttu-id="5bdbb-186">VMware 'dan Azure 'a çoğaltma yönünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="5bdbb-187">-Onay</span><span class="sxs-lookup"><span data-stu-id="5bdbb-187">-Confirm</span></span>
<span data-ttu-id="5bdbb-188">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bdbb-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdbb-189">-WhatIf</span></span>
<span data-ttu-id="5bdbb-190">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bdbb-191">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bdbb-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdbb-192">CommonParameters</span></span>
<span data-ttu-id="5bdbb-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdbb-194">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5bdbb-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdbb-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bdbb-195">INPUTS</span></span>

### <span data-ttu-id="5bdbb-196">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5bdbb-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="5bdbb-197">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="5bdbb-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5bdbb-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bdbb-198">OUTPUTS</span></span>

### <span data-ttu-id="5bdbb-199">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5bdbb-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5bdbb-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bdbb-200">NOTES</span></span>

## <span data-ttu-id="5bdbb-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bdbb-201">RELATED LINKS</span></span>
