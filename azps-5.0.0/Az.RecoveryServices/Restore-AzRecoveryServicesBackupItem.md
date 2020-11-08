---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277212"
---
# <span data-ttu-id="10c17-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="10c17-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="10c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10c17-102">SYNOPSIS</span></span>

<span data-ttu-id="10c17-103">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="10c17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10c17-104">SYNTAX</span></span>

### <span data-ttu-id="10c17-105">AzureVMParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="10c17-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c17-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c17-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c17-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="10c17-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c17-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c17-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c17-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c17-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c17-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="10c17-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c17-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="10c17-111">DESCRIPTION</span></span>

<span data-ttu-id="10c17-112">**Restore-Azrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="10c17-113">Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.</span><span class="sxs-lookup"><span data-stu-id="10c17-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="10c17-114">Geri yükleme işlemi tam sanal makineyi geri yüklemez.</span><span class="sxs-lookup"><span data-stu-id="10c17-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="10c17-115">Yönetilen diskleri, geri yükleme işlemi bittikten sonra müşteri depolama hesabına bir hedef kaynak grubuna ve yapılandırma bilgilerine geri yükler, sanal makineyi oluşturmalı ve başlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="10c17-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="10c17-116">Daha fazla bilgi için lütfen farklı olası parametre kümelerine ve parametre metnine geri gidin.</span><span class="sxs-lookup"><span data-stu-id="10c17-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="10c17-117">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="10c17-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="10c17-118">Not:-VaultId parametresine ek olarak bu cmdlet 'i başarıyla yürütmek Için-VaultLocation parametresi de kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="10c17-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="10c17-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10c17-119">EXAMPLES</span></span>

### <span data-ttu-id="10c17-120">Örnek 1: öğeyi kurtarma noktasına geri yükleme</span><span class="sxs-lookup"><span data-stu-id="10c17-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="10c17-121">İlk komut, RecoveryServices kasasından alır ve $vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="10c17-122">İkinci komut yedek öğeleri alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="10c17-123">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="10c17-124">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="10c17-125">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="10c17-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="10c17-126">Altıncı komut, kurtarma noktasından geri yüklenecek diskleri ve $restoreDiskLUNs değişkeninde depolar belirtir.</span><span class="sxs-lookup"><span data-stu-id="10c17-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="10c17-127">Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="10c17-128">Örnek 2: AzureFileShare öğesinin birden çok dosyasını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="10c17-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="10c17-129">İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="10c17-130">İkinci komut, fileshareıtem adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="10c17-131">Üçüncü komut, belirli bir yedekleme öğesi için kurtarma noktaları listesi alır.</span><span class="sxs-lookup"><span data-stu-id="10c17-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="10c17-132">Dördüncü komut, geri yüklenecek dosyaları spceifies ve $files değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="10c17-133">Son komut belirtilen dosyaları özgün konumuna geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="10c17-134">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="10c17-134">Example 3</span></span>

<span data-ttu-id="10c17-135">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="10c17-136">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="10c17-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="10c17-137">Örnek 4: yönetilen bir VM 'Yi yönetilen disk olarak geri yükleme</span><span class="sxs-lookup"><span data-stu-id="10c17-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="10c17-138">İlk komut, RecoveryServices kasasından alır ve $vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="10c17-139">İkinci komut yedek öğeyi alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="10c17-140">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="10c17-141">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="10c17-142">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="10c17-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="10c17-143">Altıncı komut, verilen hedef kaynak grubuyla yönetilen diskler olarak diskleri geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="10c17-144">Örnek 5: yönetilen VM 'Yi yönetilmeyen diskler olarak geri yükleme</span><span class="sxs-lookup"><span data-stu-id="10c17-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="10c17-145">İlk komut, RecoveryServices kasasından alır ve $vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="10c17-146">İkinci komut yedek öğeyi alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="10c17-147">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="10c17-148">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="10c17-149">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="10c17-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="10c17-150">Altıncı komut, diskleri yönetilmeyen diskler olarak geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="10c17-151">Örnek 6: yönetilmeyen VM 'Yi özgün depolama hesabını kullanarak yönetilmeyen diskler olarak geri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="10c17-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="10c17-152">İlk komut, RecoveryServices kasasından alır ve $vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="10c17-153">İkinci komut yedek öğeyi alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="10c17-154">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="10c17-155">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="10c17-156">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="10c17-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="10c17-157">Altıncı komut, VM 'nin orijinal depolama hesabını kullanarak, diskleri yönetilmeyen diskler olarak geri yükler.</span><span class="sxs-lookup"><span data-stu-id="10c17-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="10c17-158">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10c17-158">PARAMETERS</span></span>

### <span data-ttu-id="10c17-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c17-159">-DefaultProfile</span></span>

<span data-ttu-id="10c17-160">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10c17-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10c17-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="10c17-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="10c17-162">Dosya paylaşımından birden çok dosya geri yüklemesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="10c17-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="10c17-163">Dosya paylaşımı içinde geri yüklenecek öğelerin yolları.</span><span class="sxs-lookup"><span data-stu-id="10c17-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="10c17-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="10c17-164">-RecoveryPoint</span></span>

<span data-ttu-id="10c17-165">Yedekleme öğesinin geri yükleneceği kurtarma noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10c17-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="10c17-166">**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için **Get-azrecoveryservicesbackuprecoverypoint** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="10c17-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="10c17-167">-ResolveConflict</span></span>

<span data-ttu-id="10c17-168">Geri yüklenen öğenin hedefte da bulunması durumunda, üzerine yazılıp yazılmayacağını belirtmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="10c17-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="10c17-169">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10c17-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10c17-170">İne</span><span class="sxs-lookup"><span data-stu-id="10c17-170">Overwrite</span></span>
- <span data-ttu-id="10c17-171">Git</span><span class="sxs-lookup"><span data-stu-id="10c17-171">Skip</span></span>

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

### <span data-ttu-id="10c17-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="10c17-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="10c17-173">Yönetilmeyen diskler olarak geri yüklemeyi belirtmek için bu anahtarı kullanın</span><span class="sxs-lookup"><span data-stu-id="10c17-173">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="10c17-174">-RestoreDiskList</span></span>
<span data-ttu-id="10c17-175">Yedeklenen VM 'nin kurtarılacağı diskleri belirtme</span><span class="sxs-lookup"><span data-stu-id="10c17-175">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-176">-Restoreilyosdisk</span><span class="sxs-lookup"><span data-stu-id="10c17-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="10c17-177">Yalnızca yedeklenen VM disklerini geri yüklemek için bu anahtarı kullanın</span><span class="sxs-lookup"><span data-stu-id="10c17-177">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="10c17-178">-SourceFilePath</span></span>

<span data-ttu-id="10c17-179">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="10c17-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="10c17-180">Dosya paylaşımı içinde geri yüklenecek öğenin yolu.</span><span class="sxs-lookup"><span data-stu-id="10c17-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="10c17-181">-Sourcedosyatürü</span><span class="sxs-lookup"><span data-stu-id="10c17-181">-SourceFileType</span></span>

<span data-ttu-id="10c17-182">Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="10c17-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="10c17-183">Dosya paylaşımı içinde geri yüklenecek öğenin türü.</span><span class="sxs-lookup"><span data-stu-id="10c17-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="10c17-184">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10c17-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10c17-185">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="10c17-185">File</span></span>
- <span data-ttu-id="10c17-186">Directory</span><span class="sxs-lookup"><span data-stu-id="10c17-186">Directory</span></span>

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

### <span data-ttu-id="10c17-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="10c17-187">-StorageAccountName</span></span>

<span data-ttu-id="10c17-188">Aboneliğinizdeki hedef depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10c17-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="10c17-189">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c17-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="10c17-191">Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10c17-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="10c17-192">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="10c17-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-193">-Targetfilepaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="10c17-193">-TargetFileShareName</span></span>

<span data-ttu-id="10c17-194">Dosya paylaşımının geri yüklenmesi gereken dosya paylaşımı.</span><span class="sxs-lookup"><span data-stu-id="10c17-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="10c17-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="10c17-195">-TargetFolder</span></span>

<span data-ttu-id="10c17-196">Dosya paylaşımının altındaki Targetfilepaylaşımadı içinde geri yüklenmesi gereken klasör.</span><span class="sxs-lookup"><span data-stu-id="10c17-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="10c17-197">Yedeklenen içeriğin kök klasöre geri yüklenebilmesi için, hedef klasör değerlerini boş dize olarak verin.</span><span class="sxs-lookup"><span data-stu-id="10c17-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="10c17-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c17-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="10c17-199">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="10c17-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="10c17-200">Yönetilen disklerle VM yedeklemesi için geçerlidir</span><span class="sxs-lookup"><span data-stu-id="10c17-200">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="10c17-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="10c17-202">Dosya paylaşımının geri yüklenmesi gereken depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="10c17-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="10c17-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10c17-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="10c17-204">Kurtarma noktasındaki disklerin orijinal depolama hesaplarına geri yüklenebilmesi durumunda bu anahtarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="10c17-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c17-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="10c17-205">-VaultId</span></span>

<span data-ttu-id="10c17-206">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="10c17-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="10c17-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="10c17-207">-VaultLocation</span></span>

<span data-ttu-id="10c17-208">Kurtarma Hizmetleri kasasındaki konum.</span><span class="sxs-lookup"><span data-stu-id="10c17-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="10c17-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="10c17-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="10c17-210">Kurtarma Yapılandırması</span><span class="sxs-lookup"><span data-stu-id="10c17-210">Recovery config</span></span>

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

### <span data-ttu-id="10c17-211">-Onay</span><span class="sxs-lookup"><span data-stu-id="10c17-211">-Confirm</span></span>

<span data-ttu-id="10c17-212">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10c17-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10c17-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c17-213">-WhatIf</span></span>

<span data-ttu-id="10c17-214">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10c17-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="10c17-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c17-215">CommonParameters</span></span>
<span data-ttu-id="10c17-216">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10c17-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c17-217">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="10c17-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c17-218">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10c17-218">INPUTS</span></span>

### <span data-ttu-id="10c17-219">System. String</span><span class="sxs-lookup"><span data-stu-id="10c17-219">System.String</span></span>

### <span data-ttu-id="10c17-220">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="10c17-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="10c17-221">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10c17-221">OUTPUTS</span></span>

### <span data-ttu-id="10c17-222">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="10c17-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="10c17-223">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10c17-223">NOTES</span></span>

## <span data-ttu-id="10c17-224">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10c17-224">RELATED LINKS</span></span>

[<span data-ttu-id="10c17-225">Backup-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="10c17-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="10c17-226">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="10c17-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="10c17-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="10c17-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
