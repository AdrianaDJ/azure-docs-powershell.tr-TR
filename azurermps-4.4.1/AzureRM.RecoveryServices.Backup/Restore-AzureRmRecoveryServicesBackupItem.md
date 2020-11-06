---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: c12241457b78d9020e447b6f464d5623e90d52b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594197"
---
# <span data-ttu-id="cfe45-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cfe45-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="cfe45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe45-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe45-103">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cfe45-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfe45-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfe45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfe45-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe45-106">**Restore-Azurermrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cfe45-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="cfe45-107">Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.</span><span class="sxs-lookup"><span data-stu-id="cfe45-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="cfe45-108">Geri yükleme işlemi tam sanal makineyi geri yüklemez.</span><span class="sxs-lookup"><span data-stu-id="cfe45-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="cfe45-109">Disk verilerini ve yapılandırma bilgilerini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cfe45-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="cfe45-110">Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="cfe45-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="cfe45-111">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cfe45-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="cfe45-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfe45-112">EXAMPLES</span></span>

### <span data-ttu-id="cfe45-113">Örnek 1: öğeyi kurtarma noktasına geri yükleme</span><span class="sxs-lookup"><span data-stu-id="cfe45-113">Example 1: Restore an item to a recovery point</span></span>
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

<span data-ttu-id="cfe45-114">İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cfe45-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="cfe45-115">İkinci komut, V2VM adındaki yedekleme öğesini $Container alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cfe45-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="cfe45-116">Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cfe45-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="cfe45-117">Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cfe45-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="cfe45-118">Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cfe45-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="cfe45-119">Belirtilen tarih aralığı son 7 gündür.</span><span class="sxs-lookup"><span data-stu-id="cfe45-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="cfe45-120">Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="cfe45-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="cfe45-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfe45-121">PARAMETERS</span></span>

### <span data-ttu-id="cfe45-122">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cfe45-122">-RecoveryPoint</span></span>
<span data-ttu-id="cfe45-123">Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe45-123">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="cfe45-124">**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cfe45-124">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="cfe45-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cfe45-125">-StorageAccountName</span></span>
<span data-ttu-id="cfe45-126">Aboneliğinizdeki hedef depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe45-126">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="cfe45-127">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="cfe45-127">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="cfe45-128">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe45-128">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="cfe45-129">Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe45-129">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="cfe45-130">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="cfe45-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="cfe45-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe45-131">-DefaultProfile</span></span>
<span data-ttu-id="cfe45-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cfe45-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe45-133">CommonParameters</span></span>
<span data-ttu-id="cfe45-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfe45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe45-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe45-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe45-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfe45-136">INPUTS</span></span>

### <span data-ttu-id="cfe45-137">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="cfe45-137">RecoveryPointBase</span></span>
<span data-ttu-id="cfe45-138">' RecoveryPoint ' parametresi ardışık düzenin ' RecoveryPointBase ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cfe45-138">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="cfe45-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfe45-139">OUTPUTS</span></span>

### <span data-ttu-id="cfe45-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="cfe45-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="cfe45-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfe45-141">NOTES</span></span>

## <span data-ttu-id="cfe45-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfe45-142">RELATED LINKS</span></span>

[<span data-ttu-id="cfe45-143">Backup-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="cfe45-143">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="cfe45-144">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="cfe45-144">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="cfe45-145">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cfe45-145">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


