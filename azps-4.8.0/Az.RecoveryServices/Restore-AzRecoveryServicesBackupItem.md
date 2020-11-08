---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109372"
---
# <span data-ttu-id="2cfc4-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2cfc4-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="2cfc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cfc4-102">SYNOPSIS</span></span>

<span data-ttu-id="2cfc4-103">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="2cfc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cfc4-104">SYNTAX</span></span>

### <span data-ttu-id="2cfc4-105">AzureVMParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2cfc4-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cfc4-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfc4-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cfc4-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfc4-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cfc4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cfc4-108">DESCRIPTION</span></span>

<span data-ttu-id="2cfc4-109">**Restore-Azrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="2cfc4-110">Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="2cfc4-111">Geri yükleme işlemi tam sanal makineyi geri yüklemez.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="2cfc4-112">Yönetilen diskleri, geri yükleme işlemi bittikten sonra müşteri depolama hesabına bir hedef kaynak grubuna ve yapılandırma bilgilerine geri yükler, sanal makineyi oluşturmalı ve başlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="2cfc4-113">Daha fazla bilgi için lütfen farklı olası parametre kümelerine ve parametre metnine geri gidin.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="2cfc4-114">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="2cfc4-115">Not:-VaultId parametresine ek olarak bu cmdlet 'i başarıyla yürütmek Için-VaultLocation parametresi de kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="2cfc4-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cfc4-116">EXAMPLES</span></span>

### <span data-ttu-id="2cfc4-117">Örnek 1: öğeyi kurtarma noktasına geri yükleme</span><span class="sxs-lookup"><span data-stu-id="2cfc4-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="2cfc4-118">İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2cfc4-119">İkinci komut, V2VM adındaki yedekleme öğesini $Container alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="2cfc4-120">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2cfc4-121">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2cfc4-122">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="2cfc4-123">Belirtilen tarih aralığı son 7 gündür.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="2cfc4-124">Yedinci komutu, kurtarma noktasından hangi disklerin geri yükleneceği ve $restoreDiskLUNs değişkeninde sakladığı diskleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="2cfc4-125">Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="2cfc4-126">Örnek 2: AzureFileShare öğesinin birden çok dosyasını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="2cfc4-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="2cfc4-127">İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2cfc4-128">İkinci komut, fileshareıtem adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="2cfc4-129">Üçüncü komut, belirli bir yedekleme öğesi için kurtarma noktaları listesi alır.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="2cfc4-130">Dördüncü komut, geri yüklenecek dosyaları spceifies ve $files değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="2cfc4-131">Son komut belirtilen dosyaları özgün konumuna geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="2cfc4-132">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2cfc4-132">Example 3</span></span>

<span data-ttu-id="2cfc4-133">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="2cfc4-134">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="2cfc4-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="2cfc4-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cfc4-135">PARAMETERS</span></span>

### <span data-ttu-id="2cfc4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfc4-136">-DefaultProfile</span></span>

<span data-ttu-id="2cfc4-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cfc4-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="2cfc4-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="2cfc4-139">Dosya paylaşımından birden çok dosya geri yüklemesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="2cfc4-140">Dosya paylaşımı içinde geri yüklenecek öğelerin yolları.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-140">The paths of the items to be restored within the file share.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfc4-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2cfc4-141">-RecoveryPoint</span></span>

<span data-ttu-id="2cfc4-142">Yedekleme öğesinin geri yükleneceği kurtarma noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="2cfc4-143">**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için **Get-azrecoveryservicesbackuprecoverypoint** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="2cfc4-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="2cfc4-144">-ResolveConflict</span></span>

<span data-ttu-id="2cfc4-145">Geri yüklenen öğenin hedefte da bulunması durumunda, üzerine yazılıp yazılmayacağını belirtmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="2cfc4-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2cfc4-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfc4-147">İne</span><span class="sxs-lookup"><span data-stu-id="2cfc4-147">Overwrite</span></span>
- <span data-ttu-id="2cfc4-148">Git</span><span class="sxs-lookup"><span data-stu-id="2cfc4-148">Skip</span></span>

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

### <span data-ttu-id="2cfc4-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="2cfc4-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="2cfc4-150">Yönetilmeyen diskler olarak geri yüklemeyi belirtmek için bu anahtarı kullanın</span><span class="sxs-lookup"><span data-stu-id="2cfc4-150">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="2cfc4-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="2cfc4-151">-RestoreDiskList</span></span>
<span data-ttu-id="2cfc4-152">Yedeklenen VM 'nin kurtarılacağı diskleri belirtme</span><span class="sxs-lookup"><span data-stu-id="2cfc4-152">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfc4-153">-Restoreilyosdisk</span><span class="sxs-lookup"><span data-stu-id="2cfc4-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="2cfc4-154">Yalnızca yedeklenen VM disklerini geri yüklemek için bu anahtarı kullanın</span><span class="sxs-lookup"><span data-stu-id="2cfc4-154">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="2cfc4-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="2cfc4-155">-SourceFilePath</span></span>

<span data-ttu-id="2cfc4-156">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="2cfc4-157">Dosya paylaşımı içinde geri yüklenecek öğenin yolu.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-157">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="2cfc4-158">-Sourcedosyatürü</span><span class="sxs-lookup"><span data-stu-id="2cfc4-158">-SourceFileType</span></span>

<span data-ttu-id="2cfc4-159">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="2cfc4-160">Dosya paylaşımı içinde geri yüklenecek öğenin türü.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="2cfc4-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2cfc4-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfc4-162">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="2cfc4-162">File</span></span>
- <span data-ttu-id="2cfc4-163">Directory</span><span class="sxs-lookup"><span data-stu-id="2cfc4-163">Directory</span></span>

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

### <span data-ttu-id="2cfc4-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2cfc4-164">-StorageAccountName</span></span>

<span data-ttu-id="2cfc4-165">Aboneliğinizdeki hedef depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="2cfc4-166">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="2cfc4-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfc4-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="2cfc4-168">Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="2cfc4-169">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="2cfc4-170">-Targetfilepaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="2cfc4-170">-TargetFileShareName</span></span>

<span data-ttu-id="2cfc4-171">Dosya paylaşımının geri yüklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-171">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="2cfc4-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="2cfc4-172">-TargetFolder</span></span>

<span data-ttu-id="2cfc4-173">Dosya paylaşımının altındaki Targetfilepaylaşımadı içinde geri yüklenmesi gereken klasör.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="2cfc4-174">Yedeklenen içeriğin kök klasöre geri yüklenebilmesi için, hedef klasör değerlerini boş dize olarak verin.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="2cfc4-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfc4-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="2cfc4-176">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="2cfc4-177">Yönetilen disklerle VM yedeklemesi için geçerlidir</span><span class="sxs-lookup"><span data-stu-id="2cfc4-177">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="2cfc4-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2cfc4-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="2cfc4-179">Dosya paylaşımının geri yüklenmesi gereken depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-179">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="2cfc4-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2cfc4-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="2cfc4-181">Kurtarma noktasındaki disklerin orijinal depolama hesaplarına geri yüklenebilmesi durumunda bu anahtarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="2cfc4-182">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2cfc4-182">-VaultId</span></span>

<span data-ttu-id="2cfc4-183">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-183">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2cfc4-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="2cfc4-184">-VaultLocation</span></span>

<span data-ttu-id="2cfc4-185">Kurtarma Hizmetleri kasasındaki konum.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-185">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2cfc4-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="2cfc4-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="2cfc4-187">Kurtarma Yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2cfc4-187">Recovery config</span></span>

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

### <span data-ttu-id="2cfc4-188">-Onay</span><span class="sxs-lookup"><span data-stu-id="2cfc4-188">-Confirm</span></span>

<span data-ttu-id="2cfc4-189">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cfc4-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cfc4-190">-WhatIf</span></span>

<span data-ttu-id="2cfc4-191">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-191">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="2cfc4-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfc4-192">CommonParameters</span></span>
<span data-ttu-id="2cfc4-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfc4-194">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2cfc4-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfc4-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cfc4-195">INPUTS</span></span>

### <span data-ttu-id="2cfc4-196">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfc4-196">System.String</span></span>

### <span data-ttu-id="2cfc4-197">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="2cfc4-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2cfc4-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cfc4-198">OUTPUTS</span></span>

### <span data-ttu-id="2cfc4-199">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="2cfc4-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2cfc4-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cfc4-200">NOTES</span></span>

## <span data-ttu-id="2cfc4-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cfc4-201">RELATED LINKS</span></span>

[<span data-ttu-id="2cfc4-202">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="2cfc4-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="2cfc4-203">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="2cfc4-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="2cfc4-204">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2cfc4-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
