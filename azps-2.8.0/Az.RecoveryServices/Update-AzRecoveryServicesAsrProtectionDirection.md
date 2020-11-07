---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 9dd28cd3a05db15cef64a1e6023b1684909fdc13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932949"
---
# <span data-ttu-id="5fc80-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="5fc80-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="5fc80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc80-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc80-103">Belirtilen çoğaltma korumalı öğesi veya kurtarma planı için çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="5fc80-104">Yinelenen öğeyi veya kurtarma planını geri çevirmek/geri çevirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5fc80-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="5fc80-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fc80-105">SYNTAX</span></span>

### <span data-ttu-id="5fc80-106">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5fc80-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc80-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="5fc80-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc80-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5fc80-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc80-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="5fc80-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc80-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5fc80-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc80-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5fc80-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc80-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fc80-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc80-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5fc80-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc80-114">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="5fc80-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fc80-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fc80-115">DESCRIPTION</span></span>
<span data-ttu-id="5fc80-116">**Update-AzRecoveryServicesAsrProtectionDirection** cmdlet 'i, bir yürütme yük devretmesi işlemi tamamlandıktan sonra belirtilen Azure Site Recovery nesnesinin çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="5fc80-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fc80-117">EXAMPLES</span></span>

### <span data-ttu-id="5fc80-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5fc80-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="5fc80-119">Belirtilen kurtarma planı için yön güncelleştirme işlemini başlatın ve işlemi izlemek için kullanılan ASR iş nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5fc80-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="5fc80-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5fc80-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="5fc80-121">Koruma kapsayıcısı eşlemesi ve önbellek depolama alanı (VM ile aynı bölgede) kullanılarak tanımlanan hedef Azure bölgesinde belirtilen çoğaltma korumalı öğesi için güncelleştirme yönü işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="5fc80-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="5fc80-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5fc80-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="5fc80-123">Koruma kapsayıcısı eşleme tarafından tanımlanan hedef Azure bölgesinde belirtilen çoğaltma korumalı öğesi için korumayı Güncelleştir işlemini başlatın ve sağlanan disk çoğaltma yapılandırması sağlanır.</span><span class="sxs-lookup"><span data-stu-id="5fc80-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="5fc80-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fc80-124">PARAMETERS</span></span>

### <span data-ttu-id="5fc80-125">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5fc80-125">-Account</span></span>
<span data-ttu-id="5fc80-126">Gerekirse Mobility hizmetini göndermek için kullanılacak farklı hesapla hesabı.</span><span class="sxs-lookup"><span data-stu-id="5fc80-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="5fc80-127">ASR yapısı 'nda farklı Run as hesapları listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5fc80-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="5fc80-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5fc80-128">-AzureToAzure</span></span>
<span data-ttu-id="5fc80-129">{{Fill AzureToAzure açıklama}}</span><span class="sxs-lookup"><span data-stu-id="5fc80-129">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="5fc80-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fc80-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="5fc80-131">{{Fill AzureToAzureDiskReplicationConfiguration açıklama}}</span><span class="sxs-lookup"><span data-stu-id="5fc80-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

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

### <span data-ttu-id="5fc80-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="5fc80-132">-AzureToVMware</span></span>
<span data-ttu-id="5fc80-133">{{Fill AzureToVMware açıklama}}</span><span class="sxs-lookup"><span data-stu-id="5fc80-133">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="5fc80-134">-DataStore</span><span class="sxs-lookup"><span data-stu-id="5fc80-134">-DataStore</span></span>
<span data-ttu-id="5fc80-135">Vmdisk için kullanılacak VMware veri deposu.</span><span class="sxs-lookup"><span data-stu-id="5fc80-135">The VMware datastore to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="5fc80-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc80-136">-DefaultProfile</span></span>
<span data-ttu-id="5fc80-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5fc80-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5fc80-138">-Yön</span><span class="sxs-lookup"><span data-stu-id="5fc80-138">-Direction</span></span>
<span data-ttu-id="5fc80-139">Bir yük devretme sonrası güncelleştirme işleminde kullanılacak yönü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="5fc80-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5fc80-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5fc80-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5fc80-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="5fc80-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5fc80-142">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="5fc80-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="5fc80-143">-HyperVToAzure</span></span>
<span data-ttu-id="5fc80-144">Yeniden başlatıldıktan sonra Hyper-V sanal makinesini yeniden koruyun.</span><span class="sxs-lookup"><span data-stu-id="5fc80-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="5fc80-145">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5fc80-145">-LogStorageAccountId</span></span>
<span data-ttu-id="5fc80-146">VM 'lerin çoğaltma günlüğünün depolanacağı depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="5fc80-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="5fc80-147">-MasterTarget</span></span>
<span data-ttu-id="5fc80-148">Ana hedef sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="5fc80-148">Master Target Server Details.</span></span>

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

### <span data-ttu-id="5fc80-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="5fc80-149">-ProcessServer</span></span>
<span data-ttu-id="5fc80-150">Çoğaltma için kullanılacak sunucu.</span><span class="sxs-lookup"><span data-stu-id="5fc80-150">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="5fc80-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5fc80-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="5fc80-152">Çoğaltma için kullanılacak koruma containerMapping.</span><span class="sxs-lookup"><span data-stu-id="5fc80-152">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="5fc80-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5fc80-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="5fc80-154">Yük devretmenin ardından sanal makinenin oluşturulması gereken kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="5fc80-154">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="5fc80-155">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5fc80-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="5fc80-156">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="5fc80-157">-Recoverybootdiagstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="5fc80-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="5fc80-158">Kurtarma Azure VM için önyükleme tanılaması depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="5fc80-159">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="5fc80-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="5fc80-160">Bu sanal makinenin yük devretmesine yönelik kurtarma bulut hizmetinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5fc80-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="5fc80-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5fc80-161">-RecoveryPlan</span></span>
<span data-ttu-id="5fc80-162">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-162">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="5fc80-163">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="5fc80-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="5fc80-164">Korumalı VM için kurtarma resourceGroup ID.</span><span class="sxs-lookup"><span data-stu-id="5fc80-164">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="5fc80-165">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="5fc80-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5fc80-166">ASR çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-166">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="5fc80-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="5fc80-167">-RetentionVolume</span></span>
<span data-ttu-id="5fc80-168">Ana hedef sunucusundaki bekletme birimi kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="5fc80-168">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="5fc80-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="5fc80-169">-VmmToVmm</span></span>
<span data-ttu-id="5fc80-170">İki VMM yönetimli Hyper-V sitesi arasında korunan Hyper-V sanal makinesinin yük devri için çoğaltma yönünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5fc80-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="5fc80-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="5fc80-171">-VMwareToAzure</span></span>
<span data-ttu-id="5fc80-172">VMware 'dan Azure 'a çoğaltma yönünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5fc80-172">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="5fc80-173">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fc80-173">-Confirm</span></span>
<span data-ttu-id="5fc80-174">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fc80-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fc80-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fc80-175">-WhatIf</span></span>
<span data-ttu-id="5fc80-176">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fc80-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fc80-177">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5fc80-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fc80-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc80-178">CommonParameters</span></span>
<span data-ttu-id="5fc80-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fc80-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc80-180">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc80-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc80-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fc80-181">INPUTS</span></span>

### <span data-ttu-id="5fc80-182">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5fc80-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="5fc80-183">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="5fc80-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5fc80-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fc80-184">OUTPUTS</span></span>

### <span data-ttu-id="5fc80-185">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5fc80-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5fc80-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fc80-186">NOTES</span></span>

## <span data-ttu-id="5fc80-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fc80-187">RELATED LINKS</span></span>
