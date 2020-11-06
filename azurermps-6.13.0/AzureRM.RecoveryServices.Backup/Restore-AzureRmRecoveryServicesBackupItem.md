---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572677"
---
# <span data-ttu-id="a0bc5-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a0bc5-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a0bc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a0bc5-103">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0bc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0bc5-104">SYNTAX</span></span>

### <span data-ttu-id="a0bc5-105">AzureVMParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0bc5-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0bc5-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0bc5-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0bc5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0bc5-107">DESCRIPTION</span></span>
<span data-ttu-id="a0bc5-108">**Restore-Azurermrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="a0bc5-109">Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="a0bc5-110">Geri yükleme işlemi tam sanal makineyi geri yüklemez.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="a0bc5-111">Disk verilerini ve yapılandırma bilgilerini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="a0bc5-112">Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="a0bc5-113">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a0bc5-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0bc5-114">EXAMPLES</span></span>

### <span data-ttu-id="a0bc5-115">Örnek 1: öğeyi kurtarma noktasına geri yükleme</span><span class="sxs-lookup"><span data-stu-id="a0bc5-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="a0bc5-116">İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a0bc5-117">İkinci komut, V2VM adındaki yedekleme öğesini $Container alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a0bc5-118">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="a0bc5-119">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="a0bc5-120">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="a0bc5-121">Belirtilen tarih aralığı son 7 gündür.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="a0bc5-122">Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="a0bc5-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0bc5-123">PARAMETERS</span></span>

### <span data-ttu-id="a0bc5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0bc5-124">-DefaultProfile</span></span>
<span data-ttu-id="a0bc5-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bc5-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a0bc5-126">-RecoveryPoint</span></span>
<span data-ttu-id="a0bc5-127">Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="a0bc5-128">**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0bc5-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="a0bc5-129">-ResolveConflict</span></span>
<span data-ttu-id="a0bc5-130">Geri yüklenen öğenin hedefte da bulunması durumunda, üzerine yazılıp yazılmayacağını belirtmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bc5-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="a0bc5-131">-SourceFilePath</span></span>
<span data-ttu-id="a0bc5-132">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a0bc5-133">Dosya paylaşımı içinde geri yüklenecek öğenin yolu.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="a0bc5-134">-Sourcedosyatürü</span><span class="sxs-lookup"><span data-stu-id="a0bc5-134">-SourceFileType</span></span>
<span data-ttu-id="a0bc5-135">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a0bc5-136">Dosya paylaşımı içinde geri yüklenecek öğenin yolu.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bc5-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a0bc5-137">-StorageAccountName</span></span>
<span data-ttu-id="a0bc5-138">Aboneliğinizdeki hedef depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="a0bc5-139">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bc5-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0bc5-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="a0bc5-141">Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="a0bc5-142">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bc5-143">-Targetfilepaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="a0bc5-143">-TargetFileShareName</span></span>
<span data-ttu-id="a0bc5-144">Dosya paylaşımının geri yüklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="a0bc5-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="a0bc5-145">-TargetFolder</span></span>
<span data-ttu-id="a0bc5-146">Dosya paylaşımının altındaki Targetfilepaylaşımadı içinde geri yüklenmesi gereken klasör. kök klasör altında geri yüklemek için değişkeni boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="a0bc5-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0bc5-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="a0bc5-148">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a0bc5-149">Yönetilen disklerle VM yedeklemesi için geçerlidir</span><span class="sxs-lookup"><span data-stu-id="a0bc5-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="a0bc5-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a0bc5-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="a0bc5-151">Dosya paylaşımının geri yüklenmesi gereken depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="a0bc5-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0bc5-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="a0bc5-153">Kurtarma noktasındaki disklerin orijinal depolama hesaplarına geri yüklenebilmesi durumunda bu anahtarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="a0bc5-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a0bc5-154">-VaultId</span></span>
<span data-ttu-id="a0bc5-155">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a0bc5-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="a0bc5-156">-VaultLocation</span></span>
<span data-ttu-id="a0bc5-157">Kurtarma Hizmetleri kasasındaki konum.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a0bc5-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0bc5-158">-Confirm</span></span>
<span data-ttu-id="a0bc5-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0bc5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0bc5-160">-WhatIf</span></span>
<span data-ttu-id="a0bc5-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0bc5-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0bc5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0bc5-163">CommonParameters</span></span>
<span data-ttu-id="a0bc5-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0bc5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0bc5-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0bc5-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0bc5-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0bc5-166">INPUTS</span></span>

### <span data-ttu-id="a0bc5-167">System. String</span><span class="sxs-lookup"><span data-stu-id="a0bc5-167">System.String</span></span>
<span data-ttu-id="a0bc5-168">Parametreler: VaultId (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0bc5-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="a0bc5-169">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a0bc5-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="a0bc5-170">Parametreler: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0bc5-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="a0bc5-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0bc5-171">OUTPUTS</span></span>

### <span data-ttu-id="a0bc5-172">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="a0bc5-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a0bc5-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0bc5-173">NOTES</span></span>

## <span data-ttu-id="a0bc5-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0bc5-174">RELATED LINKS</span></span>

[<span data-ttu-id="a0bc5-175">Backup-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="a0bc5-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="a0bc5-176">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="a0bc5-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="a0bc5-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a0bc5-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


