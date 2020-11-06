---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 13d1829326695e2860caf99bf002dcf5da31caac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587459"
---
# <span data-ttu-id="19d35-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="19d35-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="19d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19d35-102">SYNOPSIS</span></span>
<span data-ttu-id="19d35-103">Belirtilen çoğaltma korumalı öğesi veya kurtarma planı için çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19d35-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="19d35-104">Yinelenen öğeyi veya kurtarma planını geri çevirmek/geri çevirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="19d35-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19d35-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19d35-105">SYNTAX</span></span>

### <span data-ttu-id="19d35-106">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19d35-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d35-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="19d35-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19d35-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="19d35-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d35-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="19d35-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d35-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="19d35-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d35-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="19d35-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d35-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19d35-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d35-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="19d35-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d35-114">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="19d35-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19d35-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="19d35-115">DESCRIPTION</span></span>
<span data-ttu-id="19d35-116">**Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet 'i, bir yürütme yük devretmesi işlemi tamamlandıktan sonra belirtilen Azure Site Recovery nesnesinin çoğaltma yönünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19d35-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="19d35-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19d35-117">EXAMPLES</span></span>

### <span data-ttu-id="19d35-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19d35-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="19d35-119">Belirtilen kurtarma planı için yön güncelleştirme işlemini başlatın ve işlemi izlemek için kullanılan ASR iş nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="19d35-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="19d35-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="19d35-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="19d35-121">Koruma kapsayıcısı eşlemesi ve önbellek depolama alanı (VM ile aynı bölgede) kullanılarak tanımlanan hedef Azure bölgesinde belirtilen çoğaltma korumalı öğesi için güncelleştirme yönü işlemini başlatın.</span><span class="sxs-lookup"><span data-stu-id="19d35-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="19d35-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="19d35-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="19d35-123">Koruma kapsayıcısı eşleme tarafından tanımlanan hedef Azure bölgesinde belirtilen çoğaltma korumalı öğesi için korumayı Güncelleştir işlemini başlatın ve sağlanan disk çoğaltma yapılandırması sağlanır.</span><span class="sxs-lookup"><span data-stu-id="19d35-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="19d35-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19d35-124">PARAMETERS</span></span>

### <span data-ttu-id="19d35-125">-Hesap</span><span class="sxs-lookup"><span data-stu-id="19d35-125">-Account</span></span>
<span data-ttu-id="19d35-126">Gerekirse Mobility hizmetini göndermek için kullanılacak farklı hesapla hesabı.</span><span class="sxs-lookup"><span data-stu-id="19d35-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="19d35-127">ASR yapısı 'nda farklı Run as hesapları listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="19d35-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="19d35-128">-AzureToAzure</span></span>
<span data-ttu-id="19d35-129">İki Azure bölgesi arasındaki çoğaltılmış Azure sanal makineleri için çoğaltma yönünün güncelleştirildiğini belirten geçiş parametresi.</span><span class="sxs-lookup"><span data-stu-id="19d35-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="19d35-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="19d35-131">Çoğaltılacak sanal makine disklerinin listesini ve diski çoğaltmak için kullanılacak önbellek depolama hesabını ve kurtarma depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d35-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="19d35-132">-AzureToVMware</span></span>
<span data-ttu-id="19d35-133">Azure 'dan VMware 'ye çoğaltma yönünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="19d35-133">Update replication direction from Azure to Vmware.</span></span>

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

### <span data-ttu-id="19d35-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="19d35-134">-Confirm</span></span>
<span data-ttu-id="19d35-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19d35-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d35-136">-DataStore</span><span class="sxs-lookup"><span data-stu-id="19d35-136">-DataStore</span></span>
<span data-ttu-id="19d35-137">Vmdisk için kullanılacak VMware veri deposu.</span><span class="sxs-lookup"><span data-stu-id="19d35-137">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d35-138">-DefaultProfile</span></span>
<span data-ttu-id="19d35-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19d35-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="19d35-140">-Yön</span><span class="sxs-lookup"><span data-stu-id="19d35-140">-Direction</span></span>
<span data-ttu-id="19d35-141">Bir yük devretme sonrası güncelleştirme işleminde kullanılacak yönü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d35-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="19d35-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19d35-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19d35-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="19d35-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="19d35-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="19d35-144">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-145">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="19d35-145">-HyperVToAzure</span></span>
<span data-ttu-id="19d35-146">Yeniden başlatıldıktan sonra Hyper-V sanal makinesini yeniden koruyun.</span><span class="sxs-lookup"><span data-stu-id="19d35-146">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="19d35-147">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="19d35-147">-LogStorageAccountId</span></span>
<span data-ttu-id="19d35-148">VM 'lerin çoğaltma günlüğünün depolanacağı depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d35-148">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-149">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="19d35-149">-MasterTarget</span></span>
<span data-ttu-id="19d35-150">Ana hedef sunucusu ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="19d35-150">Master Target Server Details.</span></span>

```yaml
Type: ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="19d35-151">-ProcessServer</span></span>
<span data-ttu-id="19d35-152">Çoğaltma için kullanılacak sunucu.</span><span class="sxs-lookup"><span data-stu-id="19d35-152">Process Server to be used for replication.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-153">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="19d35-153">-ProtectionContainerMapping</span></span>
<span data-ttu-id="19d35-154">Çoğaltma için kullanılacak koruma containerMapping.</span><span class="sxs-lookup"><span data-stu-id="19d35-154">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-155">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="19d35-155">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="19d35-156">Yük devretmenin ardından sanal makinenin oluşturulması gereken kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="19d35-156">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-157">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="19d35-157">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="19d35-158">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d35-158">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-159">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="19d35-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="19d35-160">Bu sanal makinenin yük devretmesine yönelik kurtarma bulut hizmetinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="19d35-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="19d35-161">-RecoveryPlan</span></span>
<span data-ttu-id="19d35-162">ASR kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d35-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-163">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="19d35-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="19d35-164">Korumalı VM için kurtarma resourceGroup ID.</span><span class="sxs-lookup"><span data-stu-id="19d35-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-165">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="19d35-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="19d35-166">ASR çoğaltması korumalı öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d35-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="19d35-167">-RetentionVolume</span></span>
<span data-ttu-id="19d35-168">Ana hedef sunucusundaki bekletme birimi kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="19d35-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d35-169">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="19d35-169">-VMwareToAzure</span></span>
<span data-ttu-id="19d35-170">VMware 'dan Azure 'a çoğaltma yönünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="19d35-170">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="19d35-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="19d35-171">-VmmToVmm</span></span>
<span data-ttu-id="19d35-172">İki VMM yönetimli Hyper-V sitesi arasında korunan Hyper-V sanal makinesinin yük devri için çoğaltma yönünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="19d35-172">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="19d35-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d35-173">-WhatIf</span></span>
<span data-ttu-id="19d35-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19d35-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19d35-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19d35-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19d35-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d35-176">CommonParameters</span></span>
<span data-ttu-id="19d35-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19d35-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d35-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d35-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d35-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19d35-179">INPUTS</span></span>

### <span data-ttu-id="19d35-180">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="19d35-180">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="19d35-181">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="19d35-181">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="19d35-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19d35-182">OUTPUTS</span></span>

### <span data-ttu-id="19d35-183">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="19d35-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="19d35-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19d35-184">NOTES</span></span>

## <span data-ttu-id="19d35-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19d35-185">RELATED LINKS</span></span>
