---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932964"
---
# <span data-ttu-id="cc15b-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cc15b-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="cc15b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc15b-102">SYNOPSIS</span></span>

<span data-ttu-id="cc15b-103">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cc15b-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="cc15b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc15b-104">SYNTAX</span></span>

### <span data-ttu-id="cc15b-105">AzureVMParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cc15b-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc15b-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc15b-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc15b-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc15b-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc15b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc15b-108">DESCRIPTION</span></span>

<span data-ttu-id="cc15b-109">**Restore-Azrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cc15b-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="cc15b-110">Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.</span><span class="sxs-lookup"><span data-stu-id="cc15b-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="cc15b-111">Geri yükleme işlemi tam sanal makineyi geri yüklemez.</span><span class="sxs-lookup"><span data-stu-id="cc15b-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="cc15b-112">Disk verilerini ve yapılandırma bilgilerini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cc15b-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="cc15b-113">Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="cc15b-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="cc15b-114">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cc15b-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="cc15b-115">Not:-VaultId parametresine ek olarak bu cmdlet 'i başarıyla yürütmek Için-VaultLocation parametresi de kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cc15b-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="cc15b-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc15b-116">EXAMPLES</span></span>

### <span data-ttu-id="cc15b-117">Örnek 1: öğeyi kurtarma noktasına geri yükleme</span><span class="sxs-lookup"><span data-stu-id="cc15b-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="cc15b-118">İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cc15b-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="cc15b-119">İkinci komut, V2VM adındaki yedekleme öğesini $Container alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cc15b-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="cc15b-120">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cc15b-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="cc15b-121">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cc15b-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="cc15b-122">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cc15b-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="cc15b-123">Belirtilen tarih aralığı son 7 gündür.</span><span class="sxs-lookup"><span data-stu-id="cc15b-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="cc15b-124">Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cc15b-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="cc15b-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc15b-125">PARAMETERS</span></span>

### <span data-ttu-id="cc15b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc15b-126">-DefaultProfile</span></span>

<span data-ttu-id="cc15b-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc15b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc15b-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cc15b-128">-RecoveryPoint</span></span>

<span data-ttu-id="cc15b-129">Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc15b-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="cc15b-130">**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için **Get-azrecoveryservicesbackuprecoverypoint** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cc15b-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="cc15b-131">-ResolveConflict</span></span>

<span data-ttu-id="cc15b-132">Geri yüklenen öğenin hedefte da bulunması durumunda, üzerine yazılıp yazılmayacağını belirtmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="cc15b-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="cc15b-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cc15b-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc15b-134">İne</span><span class="sxs-lookup"><span data-stu-id="cc15b-134">Overwrite</span></span>
- <span data-ttu-id="cc15b-135">Git</span><span class="sxs-lookup"><span data-stu-id="cc15b-135">Skip</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="cc15b-136">-SourceFilePath</span></span>

<span data-ttu-id="cc15b-137">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cc15b-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="cc15b-138">Dosya paylaşımı içinde geri yüklenecek öğenin yolu.</span><span class="sxs-lookup"><span data-stu-id="cc15b-138">The path of the item to be restored within the file share.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-139">-Sourcedosyatürü</span><span class="sxs-lookup"><span data-stu-id="cc15b-139">-SourceFileType</span></span>

<span data-ttu-id="cc15b-140">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cc15b-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="cc15b-141">Dosya paylaşımı içinde geri yüklenecek öğenin türü.</span><span class="sxs-lookup"><span data-stu-id="cc15b-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="cc15b-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cc15b-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc15b-143">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="cc15b-143">File</span></span>
- <span data-ttu-id="cc15b-144">Directory</span><span class="sxs-lookup"><span data-stu-id="cc15b-144">Directory</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cc15b-145">-StorageAccountName</span></span>

<span data-ttu-id="cc15b-146">Aboneliğinizdeki hedef depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc15b-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="cc15b-147">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="cc15b-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc15b-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="cc15b-149">Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc15b-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="cc15b-150">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="cc15b-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-151">-Targetfilepaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="cc15b-151">-TargetFileShareName</span></span>

<span data-ttu-id="cc15b-152">Dosya paylaşımının geri yüklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="cc15b-152">The File Share to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="cc15b-153">-TargetFolder</span></span>

<span data-ttu-id="cc15b-154">Dosya paylaşımının altındaki Targetfilepaylaşımadı içinde geri yüklenmesi gereken klasör.</span><span class="sxs-lookup"><span data-stu-id="cc15b-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="cc15b-155">Yedeklenen içeriğin kök klasöre geri yüklenebilmesi için, hedef klasör değerlerini boş dize olarak verin.</span><span class="sxs-lookup"><span data-stu-id="cc15b-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc15b-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="cc15b-157">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cc15b-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="cc15b-158">Yönetilen disklerle VM yedeklemesi için geçerlidir</span><span class="sxs-lookup"><span data-stu-id="cc15b-158">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cc15b-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="cc15b-160">Dosya paylaşımının geri yüklenmesi gereken depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="cc15b-160">The storage account to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc15b-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="cc15b-162">Kurtarma noktasındaki disklerin orijinal depolama hesaplarına geri yüklenebilmesi durumunda bu anahtarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="cc15b-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cc15b-163">-VaultId</span></span>

<span data-ttu-id="cc15b-164">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cc15b-164">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="cc15b-165">-VaultLocation</span></span>

<span data-ttu-id="cc15b-166">Kurtarma Hizmetleri kasasındaki konum.</span><span class="sxs-lookup"><span data-stu-id="cc15b-166">Location of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="cc15b-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="cc15b-168">Kurtarma Yapılandırması</span><span class="sxs-lookup"><span data-stu-id="cc15b-168">Recovery config</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc15b-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc15b-169">-Confirm</span></span>

<span data-ttu-id="cc15b-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc15b-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc15b-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc15b-171">-WhatIf</span></span>

<span data-ttu-id="cc15b-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc15b-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc15b-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc15b-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc15b-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc15b-174">-CommonParameters</span></span>

<span data-ttu-id="cc15b-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc15b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc15b-176">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cc15b-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc15b-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc15b-177">INPUTS</span></span>

### <span data-ttu-id="cc15b-178">System. String</span><span class="sxs-lookup"><span data-stu-id="cc15b-178">System.String</span></span>

### <span data-ttu-id="cc15b-179">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="cc15b-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="cc15b-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc15b-180">OUTPUTS</span></span>

### <span data-ttu-id="cc15b-181">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="cc15b-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="cc15b-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc15b-182">NOTES</span></span>

## <span data-ttu-id="cc15b-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc15b-183">RELATED LINKS</span></span>

[<span data-ttu-id="cc15b-184">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="cc15b-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="cc15b-185">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="cc15b-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="cc15b-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cc15b-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
