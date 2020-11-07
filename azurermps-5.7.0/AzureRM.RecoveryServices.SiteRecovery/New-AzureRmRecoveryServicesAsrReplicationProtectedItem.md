---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fab7fa9f02f70b5afa1c4c5ffcbd07a8e1706998
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763561"
---
# <span data-ttu-id="94482-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="94482-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="94482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94482-102">SYNOPSIS</span></span>
<span data-ttu-id="94482-103">Çoğaltma korumalı bir öğe oluşturarak, bir ASR korunabilir öğesi için çoğaltmayı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="94482-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94482-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94482-104">SYNTAX</span></span>

### <span data-ttu-id="94482-105">EnterpriseToEnterprise (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94482-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94482-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="94482-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94482-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="94482-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94482-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="94482-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94482-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="94482-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94482-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="94482-110">DESCRIPTION</span></span>
<span data-ttu-id="94482-111">**Yeni-Azurermrecoveryservicesasrreplicationkorunabilir** , yeni bir çoğaltma korumalı öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94482-111">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="94482-112">ASR korunabilir öğesi için yinelemeyi etkinleştirmek üzere bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="94482-112">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="94482-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94482-113">EXAMPLES</span></span>

### <span data-ttu-id="94482-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94482-114">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="94482-115">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="94482-115">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="94482-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="94482-116">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="94482-117">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure senaryosuna) döndürür.</span><span class="sxs-lookup"><span data-stu-id="94482-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="94482-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="94482-118">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="94482-119">Belirtilen ASR korunabilir öğesi için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="94482-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="94482-120">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="94482-120">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="94482-121">Belirtilen VMID için çoğaltma korumalı öğe oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini (Azure 'dan Azure 'a) döndürür.</span><span class="sxs-lookup"><span data-stu-id="94482-121">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="94482-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94482-122">PARAMETERS</span></span>

### <span data-ttu-id="94482-123">-Hesap</span><span class="sxs-lookup"><span data-stu-id="94482-123">-Account</span></span>
<span data-ttu-id="94482-124">Gerekirse Mobility hizmetini göndermek için kullanılacak farklı hesapla hesabı.</span><span class="sxs-lookup"><span data-stu-id="94482-124">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="94482-125">ASR yapısı 'nda farklı Run as hesapları listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="94482-125">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="94482-126">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="94482-126">-AzureToAzure</span></span>
<span data-ttu-id="94482-127">Yinelenen öğenin, kurtarma Azure bölgesine çoğaltma yapan bir Azure sanal makinesi olduğunu belirtmek için anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="94482-127">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-128">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="94482-128">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="94482-129">Çoğaltılacak sanal makine disklerinin listesini ve diski çoğaltmak için kullanılacak önbellek depolama hesabını ve kurtarma depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-129">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-130">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="94482-130">-AzureVmId</span></span>
<span data-ttu-id="94482-131">Çoğaltılacak Azure VM kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-131">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="94482-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="94482-132">-Confirm</span></span>
<span data-ttu-id="94482-133">İşlemi başlatmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="94482-133">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="94482-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94482-134">-DefaultProfile</span></span>
<span data-ttu-id="94482-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94482-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="94482-136">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="94482-136">-HyperVToAzure</span></span>
<span data-ttu-id="94482-137">Azure 'a çoğaltılan bir Hyper-V sanal makinesi çoğaltılmış öğenin belirtilmesi için anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="94482-137">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-138">-Includediskid</span><span class="sxs-lookup"><span data-stu-id="94482-138">-IncludeDiskId</span></span>
<span data-ttu-id="94482-139">Çoğaltmaya eklenecek disklerin listesi.</span><span class="sxs-lookup"><span data-stu-id="94482-139">The list of disks to include for replication.</span></span> <span data-ttu-id="94482-140">Varsayılan olarak tüm diskler dahildir.</span><span class="sxs-lookup"><span data-stu-id="94482-140">By default all disks are included.</span></span>

```yaml
Type: String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-141">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="94482-141">-LogStorageAccountId</span></span>
<span data-ttu-id="94482-142">Çoğaltma günlüklerinin depolanacağı günlük veya önbellek hesap kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-142">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="94482-143">-Name</span></span>
<span data-ttu-id="94482-144">ASR çoğaltması korumalı öğesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-144">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="94482-145">Adın kasa içinde benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="94482-145">The name must be unique within the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-146">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="94482-146">-OS</span></span>
<span data-ttu-id="94482-147">İşletim sistemi ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-147">Specifies the operating system family.</span></span>
<span data-ttu-id="94482-148">Bu parametre için kabul edilebilir değerler: Windows veya Linux.</span><span class="sxs-lookup"><span data-stu-id="94482-148">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-149">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="94482-149">-OSDiskName</span></span>
<span data-ttu-id="94482-150">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="94482-151">-ProcessServer</span></span>
<span data-ttu-id="94482-152">Bu makineyi çoğaltmak için kullanılacak Işlem sunucusu.</span><span class="sxs-lookup"><span data-stu-id="94482-152">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="94482-153">Yapılandırma sunucusuna karşılık gelen ASR yapısı içinde bir tane belirtmek için, sunucu listesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="94482-153">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-154">-Korunabilir öğe</span><span class="sxs-lookup"><span data-stu-id="94482-154">-ProtectableItem</span></span>
<span data-ttu-id="94482-155">Çoğaltmanın etkinleştirildiği ASR korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-155">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94482-156">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="94482-156">-ProtectionContainerMapping</span></span>
<span data-ttu-id="94482-157">Çoğaltma için kullanılacak çoğaltma ilkesine karşılık gelen ASR koruma kapsayıcısı eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-157">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-158">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="94482-158">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="94482-159">Makineyi yük devretmenin olayında kurtarmak için kullanılabilirlik kümesi KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="94482-159">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-160">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="94482-160">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="94482-161">Başarısızlık durumunda makineyi kurtarmak için Azure sanal ağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="94482-161">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-162">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="94482-162">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="94482-163">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-163">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-164">-Kurtarılan ağ adı</span><span class="sxs-lookup"><span data-stu-id="94482-164">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="94482-165">Yük devretme olayında sanal makinenin yük devretmekte olduğu, kurtarma Azure sanal ağındaki alt ağ.</span><span class="sxs-lookup"><span data-stu-id="94482-165">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-166">-Recoverycloudserviceıd</span><span class="sxs-lookup"><span data-stu-id="94482-166">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="94482-167">Bu sanal makinenin yük devretmesi için kurtarma bulut hizmetinin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-167">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-168">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="94482-168">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="94482-169">Yük devretme olayında sanal makinenin oluşturulduğu kaynak grubunun ARM tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-169">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-170">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="94482-170">-RecoveryVmName</span></span>
<span data-ttu-id="94482-171">Yük devretme sonrasında oluşturulan kurtarma VM 'sinin adı.</span><span class="sxs-lookup"><span data-stu-id="94482-171">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-172">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="94482-172">-ReplicationGroupName</span></span>
<span data-ttu-id="94482-173">Çoklu VM tutarlı kurtarma noktaları oluşturmak için kullanılacak çoğaltma grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-173">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="94482-174">Varsayılan olarak, her çoğaltma korumalı öğesi kendi bir grubunda oluşturulur ve çoklu VM uyumlu kurtarma noktaları oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="94482-174">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="94482-175">Tüm makineleri aynı çoğaltma grubuna koruyarak, bir makine grubu genelinde çok sunuculu tutarlı kurtarma noktaları oluşturmanız gerekiyorsa bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="94482-175">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-176">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="94482-176">-VMwareToAzure</span></span>
<span data-ttu-id="94482-177">Azure 'a çoğaltılacak olan bir VMware sanal makinesi ya da fiziksel sunucusu, çoğaltılmış öğeyi belirtecek şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="94482-177">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="94482-178">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="94482-178">-VmmToVmm</span></span>
<span data-ttu-id="94482-179">Yinelenen öğenin, VMM yönetilen Hyper-V siteleri arasında çoğaltılmış bir Hyper-V sanal makinesi olduğunu belirtmek için anahtar parametresi.</span><span class="sxs-lookup"><span data-stu-id="94482-179">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-180">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="94482-180">-WaitForCompletion</span></span>
<span data-ttu-id="94482-181">Cmdlet 'in işlemin tamamlanması için beklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94482-181">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94482-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94482-182">-WhatIf</span></span>
<span data-ttu-id="94482-183">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94482-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94482-184">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94482-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94482-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94482-185">CommonParameters</span></span>
<span data-ttu-id="94482-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94482-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94482-187">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94482-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94482-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94482-188">INPUTS</span></span>

### <span data-ttu-id="94482-189">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrkorunabilir öğesi</span><span class="sxs-lookup"><span data-stu-id="94482-189">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="94482-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94482-190">OUTPUTS</span></span>

### <span data-ttu-id="94482-191">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="94482-191">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="94482-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94482-192">NOTES</span></span>

## <span data-ttu-id="94482-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94482-193">RELATED LINKS</span></span>

[<span data-ttu-id="94482-194">Get-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="94482-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="94482-195">Remove-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="94482-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="94482-196">Set-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="94482-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
