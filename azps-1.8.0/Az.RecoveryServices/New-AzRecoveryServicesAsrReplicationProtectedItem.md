---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: c3c420e29d0aba3f8e64e8b5528b62dddf974984
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759657"
---
# <span data-ttu-id="de245-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="de245-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="de245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de245-102">SYNOPSIS</span></span>
<span data-ttu-id="de245-103">Çoğaltma korumalı bir öğe oluşturarak, bir ASR korunabilir öğesi için çoğaltmayı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="de245-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="de245-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de245-104">SYNTAX</span></span>

### <span data-ttu-id="de245-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="de245-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de245-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="de245-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de245-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="de245-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de245-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="de245-108">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de245-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="de245-109">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de245-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="de245-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de245-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="de245-111">DESCRIPTION</span></span>
<span data-ttu-id="de245-112">**Yeni-Azrecoveryservicesasrreplicationkorutdıtem** cmdlet 'i, yeni bir çoğaltma korumalı öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de245-112">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="de245-113">ASR korunabilir öğesi için yinelemeyi etkinleştirmek üzere bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="de245-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="de245-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de245-114">EXAMPLES</span></span>

### <span data-ttu-id="de245-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="de245-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="de245-116">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="de245-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="de245-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="de245-117">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="de245-118">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure senaryosuna) döndürür.</span><span class="sxs-lookup"><span data-stu-id="de245-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="de245-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="de245-119">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzToAzure -AzToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="de245-120">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="de245-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="de245-121">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="de245-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="de245-122">Belirtilen VMID için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="de245-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="de245-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de245-123">PARAMETERS</span></span>

### <span data-ttu-id="de245-124">-Hesap</span><span class="sxs-lookup"><span data-stu-id="de245-124">-Account</span></span>
<span data-ttu-id="de245-125">Gerekirse Mobility hizmetini göndermek için kullanılacak farklı hesapla hesabı.</span><span class="sxs-lookup"><span data-stu-id="de245-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="de245-126">ASR yapısı 'nda farklı Run as hesapları listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="de245-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="de245-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="de245-127">-AzureToAzure</span></span>
<span data-ttu-id="de245-128">{{Fill AzureToAzure açıklama}}</span><span class="sxs-lookup"><span data-stu-id="de245-128">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="de245-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="de245-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="de245-130">{{Fill AzureToAzureDiskReplicationConfiguration açıklama}}</span><span class="sxs-lookup"><span data-stu-id="de245-130">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

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

### <span data-ttu-id="de245-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="de245-131">-AzureVmId</span></span>
<span data-ttu-id="de245-132">{{Fill AzureVmId açıklama}}</span><span class="sxs-lookup"><span data-stu-id="de245-132">{{Fill AzureVmId Description}}</span></span>

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

### <span data-ttu-id="de245-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de245-133">-DefaultProfile</span></span>
<span data-ttu-id="de245-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de245-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="de245-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="de245-135">-HyperVToAzure</span></span>
<span data-ttu-id="de245-136">Azure 'a çoğaltılan bir Hyper-V sanal makinesi çoğaltılmış öğenin belirtilmesi için anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="de245-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="de245-137">-Includediskid</span><span class="sxs-lookup"><span data-stu-id="de245-137">-IncludeDiskId</span></span>
<span data-ttu-id="de245-138">Çoğaltmaya eklenecek disklerin listesi.</span><span class="sxs-lookup"><span data-stu-id="de245-138">The list of disks to include for replication.</span></span> <span data-ttu-id="de245-139">Varsayılan olarak tüm diskler dahildir.</span><span class="sxs-lookup"><span data-stu-id="de245-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-140">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="de245-140">-LogStorageAccountId</span></span>
<span data-ttu-id="de245-141">Çoğaltma günlüklerinin depolanacağı günlük veya önbellek hesap kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="de245-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="de245-142">-Name</span></span>
<span data-ttu-id="de245-143">ASR çoğaltması korumalı öğesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="de245-144">Adın kasa içinde benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="de245-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="de245-145">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="de245-145">-OS</span></span>
<span data-ttu-id="de245-146">İşletim sistemi ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-146">Specifies the operating system family.</span></span>
<span data-ttu-id="de245-147">Bu parametre için kabul edilebilir değerler: Windows veya Linux.</span><span class="sxs-lookup"><span data-stu-id="de245-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="de245-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="de245-148">-OSDiskName</span></span>
<span data-ttu-id="de245-149">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="de245-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="de245-150">-ProcessServer</span></span>
<span data-ttu-id="de245-151">Bu makineyi çoğaltmak için kullanılacak Işlem sunucusu.</span><span class="sxs-lookup"><span data-stu-id="de245-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="de245-152">Yapılandırma sunucusuna karşılık gelen ASR yapısı içinde bir tane belirtmek için, sunucu listesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="de245-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-153">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="de245-153">-ProtectableItem</span></span>
<span data-ttu-id="de245-154">Çoğaltmanın etkinleştirildiği ASR korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de245-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="de245-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="de245-156">Çoğaltma için kullanılacak çoğaltma ilkesine karşılık gelen ASR koruma kapsayıcısı eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="de245-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="de245-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="de245-158">Makineyi yük devretmenin olayında kurtarmak için kullanılabilirlik kümesi KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="de245-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="de245-159">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="de245-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="de245-160">Başarısızlık durumunda makineyi kurtarmak için Azure sanal ağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="de245-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-161">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="de245-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="de245-162">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="de245-163">-Kurtarılan ağ adı</span><span class="sxs-lookup"><span data-stu-id="de245-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="de245-164">Yük devretme olayında sanal makinenin yük devretmekte olduğu, kurtarma Azure sanal ağındaki alt ağ.</span><span class="sxs-lookup"><span data-stu-id="de245-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-165">-Recoverybootdiagstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="de245-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="de245-166">Kurtarma Azure VM için önyükleme tanılaması depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="de245-167">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="de245-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="de245-168">Bu sanal makinenin yük devretmesi için kurtarma bulut hizmetinin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="de245-169">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="de245-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="de245-170">Yük devretme olayında sanal makinenin oluşturulduğu kaynak grubunun ARM tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="de245-171">-RecoveryVmName</span></span>
<span data-ttu-id="de245-172">Yük devretme sonrasında oluşturulan kurtarma VM 'sinin adı.</span><span class="sxs-lookup"><span data-stu-id="de245-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="de245-173">-ReplicationGroupName</span></span>
<span data-ttu-id="de245-174">Çoklu VM tutarlı kurtarma noktaları oluşturmak için kullanılacak çoğaltma grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="de245-175">Varsayılan olarak, her çoğaltma korumalı öğesi kendi bir grubunda oluşturulur ve çoklu VM uyumlu kurtarma noktaları oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="de245-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="de245-176">Tüm makineleri aynı çoğaltma grubuna koruyarak, bir makine grubu genelinde çok sunuculu tutarlı kurtarma noktaları oluşturmanız gerekiyorsa bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="de245-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de245-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="de245-177">-VmmToVmm</span></span>
<span data-ttu-id="de245-178">Yinelenen öğenin, VMM yönetilen Hyper-V siteleri arasında çoğaltılmış bir Hyper-V sanal makinesi olduğunu belirtmek için anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="de245-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="de245-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="de245-179">-VMwareToAzure</span></span>
<span data-ttu-id="de245-180">Azure 'a çoğaltılacak olan bir VMware sanal makinesi ya da fiziksel sunucusu, çoğaltılmış öğeyi belirtecek şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="de245-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="de245-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="de245-181">-WaitForCompletion</span></span>
<span data-ttu-id="de245-182">Cmdlet 'in işlemin tamamlanması için beklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de245-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="de245-183">-Onay</span><span class="sxs-lookup"><span data-stu-id="de245-183">-Confirm</span></span>
<span data-ttu-id="de245-184">İşlemi başlatmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="de245-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="de245-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de245-185">-WhatIf</span></span>
<span data-ttu-id="de245-186">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de245-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de245-187">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de245-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de245-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de245-188">CommonParameters</span></span>
<span data-ttu-id="de245-189">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de245-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de245-190">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de245-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de245-191">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de245-191">INPUTS</span></span>

### <span data-ttu-id="de245-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="de245-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="de245-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de245-193">OUTPUTS</span></span>

### <span data-ttu-id="de245-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="de245-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="de245-195">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de245-195">NOTES</span></span>

## <span data-ttu-id="de245-196">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de245-196">RELATED LINKS</span></span>

[<span data-ttu-id="de245-197">Get-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="de245-197">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="de245-198">Remove-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="de245-198">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="de245-199">Set-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="de245-199">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
