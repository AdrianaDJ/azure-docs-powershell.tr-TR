---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: eb54d22f74216dc883726d34df204ce80c711a22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759621"
---
# <span data-ttu-id="0aed5-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0aed5-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="0aed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aed5-102">SYNOPSIS</span></span>
<span data-ttu-id="0aed5-103">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="0aed5-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="0aed5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0aed5-104">SYNTAX</span></span>

### <span data-ttu-id="0aed5-105">AzureVMParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0aed5-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aed5-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aed5-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0aed5-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aed5-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aed5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0aed5-108">DESCRIPTION</span></span>
<span data-ttu-id="0aed5-109">**Restore-Azrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="0aed5-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="0aed5-110">Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.</span><span class="sxs-lookup"><span data-stu-id="0aed5-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="0aed5-111">Geri yükleme işlemi tam sanal makineyi geri yüklemez.</span><span class="sxs-lookup"><span data-stu-id="0aed5-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="0aed5-112">Disk verilerini ve yapılandırma bilgilerini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="0aed5-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="0aed5-113">Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="0aed5-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="0aed5-114">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0aed5-114">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0aed5-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0aed5-115">EXAMPLES</span></span>

### <span data-ttu-id="0aed5-116">Örnek 1: öğeyi kurtarma noktasına geri yükleme</span><span class="sxs-lookup"><span data-stu-id="0aed5-116">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="0aed5-117">İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0aed5-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="0aed5-118">İkinci komut, V2VM adındaki yedekleme öğesini $Container alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0aed5-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="0aed5-119">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0aed5-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="0aed5-120">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0aed5-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="0aed5-121">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0aed5-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="0aed5-122">Belirtilen tarih aralığı son 7 gündür.</span><span class="sxs-lookup"><span data-stu-id="0aed5-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="0aed5-123">Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="0aed5-123">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="0aed5-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0aed5-124">PARAMETERS</span></span>

### <span data-ttu-id="0aed5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aed5-125">-DefaultProfile</span></span>
<span data-ttu-id="0aed5-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0aed5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aed5-127">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0aed5-127">-RecoveryPoint</span></span>
<span data-ttu-id="0aed5-128">Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0aed5-128">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="0aed5-129">**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için Get-AzRecoveryServicesBackupRecoveryPoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0aed5-129">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="0aed5-130">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="0aed5-130">-ResolveConflict</span></span>
<span data-ttu-id="0aed5-131">Geri yüklenen öğenin hedefte da bulunması durumunda, üzerine yazılıp yazılmayacağını belirtmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="0aed5-131">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

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

### <span data-ttu-id="0aed5-132">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="0aed5-132">-SourceFilePath</span></span>
<span data-ttu-id="0aed5-133">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0aed5-133">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="0aed5-134">Dosya paylaşımı içinde geri yüklenecek öğenin yolu.</span><span class="sxs-lookup"><span data-stu-id="0aed5-134">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="0aed5-135">-Sourcedosyatürü</span><span class="sxs-lookup"><span data-stu-id="0aed5-135">-SourceFileType</span></span>
<span data-ttu-id="0aed5-136">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0aed5-136">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="0aed5-137">Dosya paylaşımı içinde geri yüklenecek öğenin yolu.</span><span class="sxs-lookup"><span data-stu-id="0aed5-137">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="0aed5-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0aed5-138">-StorageAccountName</span></span>
<span data-ttu-id="0aed5-139">Aboneliğinizdeki hedef depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0aed5-139">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="0aed5-140">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="0aed5-140">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="0aed5-141">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aed5-141">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="0aed5-142">Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0aed5-142">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="0aed5-143">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="0aed5-143">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="0aed5-144">-Targetfilepaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="0aed5-144">-TargetFileShareName</span></span>
<span data-ttu-id="0aed5-145">Dosya paylaşımının geri yüklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="0aed5-145">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="0aed5-146">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="0aed5-146">-TargetFolder</span></span>
<span data-ttu-id="0aed5-147">Dosya paylaşımının altındaki Targetfilepaylaşımadı içinde geri yüklenmesi gereken klasör. kök klasör altında geri yüklemek için değişkeni boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="0aed5-147">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="0aed5-148">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aed5-148">-TargetResourceGroupName</span></span>
<span data-ttu-id="0aed5-149">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="0aed5-149">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="0aed5-150">Yönetilen disklerle VM yedeklemesi için geçerlidir</span><span class="sxs-lookup"><span data-stu-id="0aed5-150">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="0aed5-151">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0aed5-151">-TargetStorageAccountName</span></span>
<span data-ttu-id="0aed5-152">Dosya paylaşımının geri yüklenmesi gereken depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="0aed5-152">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="0aed5-153">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0aed5-153">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="0aed5-154">Kurtarma noktasındaki disklerin orijinal depolama hesaplarına geri yüklenebilmesi durumunda bu anahtarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="0aed5-154">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="0aed5-155">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0aed5-155">-VaultId</span></span>
<span data-ttu-id="0aed5-156">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0aed5-156">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0aed5-157">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="0aed5-157">-VaultLocation</span></span>
<span data-ttu-id="0aed5-158">Kurtarma Hizmetleri kasasındaki konum.</span><span class="sxs-lookup"><span data-stu-id="0aed5-158">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0aed5-159">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="0aed5-159">-WLRecoveryConfig</span></span>
<span data-ttu-id="0aed5-160">Kurtarma Yapılandırması</span><span class="sxs-lookup"><span data-stu-id="0aed5-160">Recovery config</span></span>

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

### <span data-ttu-id="0aed5-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="0aed5-161">-Confirm</span></span>
<span data-ttu-id="0aed5-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0aed5-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aed5-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aed5-163">-WhatIf</span></span>
<span data-ttu-id="0aed5-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0aed5-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0aed5-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0aed5-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aed5-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aed5-166">CommonParameters</span></span>
<span data-ttu-id="0aed5-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0aed5-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aed5-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aed5-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aed5-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0aed5-169">INPUTS</span></span>

### <span data-ttu-id="0aed5-170">System. String</span><span class="sxs-lookup"><span data-stu-id="0aed5-170">System.String</span></span>

### <span data-ttu-id="0aed5-171">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="0aed5-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="0aed5-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0aed5-172">OUTPUTS</span></span>

### <span data-ttu-id="0aed5-173">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="0aed5-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0aed5-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0aed5-174">NOTES</span></span>

## <span data-ttu-id="0aed5-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0aed5-175">RELATED LINKS</span></span>

[<span data-ttu-id="0aed5-176">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="0aed5-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0aed5-177">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="0aed5-177">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0aed5-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0aed5-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)


