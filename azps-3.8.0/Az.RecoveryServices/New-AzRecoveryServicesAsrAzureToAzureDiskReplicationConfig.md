---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: b5d369a4f67888d6b7035e81d3462e10586ca3ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104703"
---
# <span data-ttu-id="b5d02-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="b5d02-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="b5d02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d02-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d02-103">Azure sanal makine disklerinin çoğaltılacağı bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5d02-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="b5d02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5d02-104">SYNTAX</span></span>

### <span data-ttu-id="b5d02-105">AzureToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5d02-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5d02-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b5d02-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5d02-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5d02-107">DESCRIPTION</span></span>
<span data-ttu-id="b5d02-108">Bir Azure sanal makine diskini, diski çoğaltmak için kullanılacak önbellek depolama hesabına ve hedef depolama hesabına (kurtarma bölgesi) eşleyen bir disk eşleme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5d02-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="b5d02-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5d02-109">EXAMPLES</span></span>

### <span data-ttu-id="b5d02-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5d02-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="b5d02-111">Çoğaltılacak Azure sanal makine disklerinin disk eşleme nesnesi oluşturma. Azure ile Azure Etkinr arası ve yeniden korumada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5d02-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="b5d02-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b5d02-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="b5d02-113">Çoğaltılacak Azure sanal makine disklerinin yönetilen bir disk eşleme nesnesi oluşturma. Azure ile Azure Etkinr arası ve yeniden korumada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5d02-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="b5d02-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b5d02-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="b5d02-115">Azure sanal makine disklerinin çoğaltılacağı bir yönetilen disk eşleme nesnesi oluşturun. Azure ile Azure Etkinr arası ve yeniden korumada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5d02-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="b5d02-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="b5d02-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="b5d02-117">Azure sanal makine disklerinin çoğaltılması için hedef disk şifrelemesi kümesi kimliğiyle bir yönetilen disk eşleme nesnesi oluşturun. Azure ile Azure Etkinr arası ve yeniden korumada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5d02-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="b5d02-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5d02-118">PARAMETERS</span></span>

### <span data-ttu-id="b5d02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d02-119">-DefaultProfile</span></span>
<span data-ttu-id="b5d02-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5d02-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d02-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="b5d02-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="b5d02-122">Disk şifrelemesi gizli URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="b5d02-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="b5d02-124">Disk şifrelemesi Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="b5d02-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="b5d02-125">-DiskId</span></span>
<span data-ttu-id="b5d02-126">Yönetilen diskin disk kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="b5d02-127">-FailoverDiskName</span></span>
<span data-ttu-id="b5d02-128">Yerine çalışma sırasında oluşturulan diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="b5d02-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="b5d02-130">Anahtar şifreleme URL 'Sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="b5d02-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="b5d02-132">Anahtar şifreleme anahtarı kasa kolu kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-133">-Logstorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="b5d02-133">-LogStorageAccountId</span></span>
<span data-ttu-id="b5d02-134">Çoğaltma günlüklerinin depolanacağı günlük veya önbellek hesap kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="b5d02-135">-Manageddısk</span><span class="sxs-lookup"><span data-stu-id="b5d02-135">-ManagedDisk</span></span>
<span data-ttu-id="b5d02-136">Yönetilen disk için giriş olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-137">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="b5d02-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b5d02-138">Çoğaltılacak Azure depolama hesabının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="b5d02-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b5d02-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="b5d02-140">Kurtarma disklerinde kullanılacak Azure disk şifrelemesi kümesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="b5d02-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="b5d02-142">Çoğaltılmış yönetilen diskin hesap türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, Standard_SSD

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-143">-Recoveryresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="b5d02-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="b5d02-144">Çoğaltılmış yönetilen disk için kurtarma kaynağı grup kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="b5d02-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="b5d02-146">Çoğaltılmış yönetilen disk için kurtarma hedef diskini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, Standard_SSD

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="b5d02-147">-TfoDiskName</span></span>
<span data-ttu-id="b5d02-148">Yük devretme testi sırasında oluşturulan diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d02-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b5d02-149">-VhdUri</span></span>
<span data-ttu-id="b5d02-150">Bu eşlemenin karşılık geldiği diskin VHD URI 'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b5d02-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="b5d02-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5d02-151">-Confirm</span></span>
<span data-ttu-id="b5d02-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5d02-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d02-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d02-153">-WhatIf</span></span>
<span data-ttu-id="b5d02-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5d02-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d02-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5d02-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d02-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d02-156">CommonParameters</span></span>
<span data-ttu-id="b5d02-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5d02-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d02-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5d02-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d02-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5d02-159">INPUTS</span></span>

### <span data-ttu-id="b5d02-160">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b5d02-160">None</span></span>

## <span data-ttu-id="b5d02-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5d02-161">OUTPUTS</span></span>

### <span data-ttu-id="b5d02-162">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="b5d02-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="b5d02-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5d02-163">NOTES</span></span>

## <span data-ttu-id="b5d02-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5d02-164">RELATED LINKS</span></span>
