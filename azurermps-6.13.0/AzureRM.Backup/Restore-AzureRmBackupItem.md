---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: 3bbddc217bd33e303b998bfb816c9c0c65e96ce6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588604"
---
# <span data-ttu-id="e29f8-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="e29f8-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="e29f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29f8-102">SYNOPSIS</span></span>
<span data-ttu-id="e29f8-103">Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="e29f8-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e29f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e29f8-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e29f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e29f8-105">DESCRIPTION</span></span>
<span data-ttu-id="e29f8-106">**Restore-Azurermbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="e29f8-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="e29f8-107">Bu cmdlet, yedekleme kasasından geri yüklemeyi hesabınıza başlatır.</span><span class="sxs-lookup"><span data-stu-id="e29f8-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>
<span data-ttu-id="e29f8-108">Geri yükleme işlemi tam sanal makineyi geri yüklemez.</span><span class="sxs-lookup"><span data-stu-id="e29f8-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="e29f8-109">Disk verilerini ve yapılandırma bilgilerini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="e29f8-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="e29f8-110">Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="e29f8-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="e29f8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e29f8-111">EXAMPLES</span></span>

### <span data-ttu-id="e29f8-112">Örnek 1: sanal makineyi kurtarma noktasına geri yükleme</span><span class="sxs-lookup"><span data-stu-id="e29f8-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="e29f8-113">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="e29f8-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="e29f8-114">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e29f8-114">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="e29f8-115">İkinci komut, **Get-AzureRmBackupContainer** cmdlet 'ini kullanarak $Vault kasada belirtilen ada sahip bir kapsayıcı alır.</span><span class="sxs-lookup"><span data-stu-id="e29f8-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="e29f8-116">Komut bu nesneyi $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e29f8-116">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="e29f8-117">Üçüncü komut, **Get-Azurermbackupıtem** cmdlet 'ini kullanarak $Container kapsayıcısındaki kapsayıcıda alır.</span><span class="sxs-lookup"><span data-stu-id="e29f8-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="e29f8-118">Komut bu nesneyi $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e29f8-118">The command stores that object in the $BackupItem variable.</span></span>
<span data-ttu-id="e29f8-119">Dördüncü komut $BackupItem öğenin kurtarma noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="e29f8-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="e29f8-120">Komut bu nesneyi $RecoveryPoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e29f8-120">The command stores that object in the $RecoveryPoint variable.</span></span>
<span data-ttu-id="e29f8-121">Son komutu, hedef hesap adlı hesabın kurtarma $RecoveryPoint noktasını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="e29f8-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="e29f8-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e29f8-122">PARAMETERS</span></span>

### <span data-ttu-id="e29f8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29f8-123">-DefaultProfile</span></span>
<span data-ttu-id="e29f8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e29f8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e29f8-125">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e29f8-125">-RecoveryPoint</span></span>
<span data-ttu-id="e29f8-126">Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e29f8-126">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="e29f8-127">**Azurermbackuprecoverypoint** almak için Get-AzureRmBackupRecoveryPoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e29f8-127">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e29f8-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e29f8-128">-StorageAccountName</span></span>
<span data-ttu-id="e29f8-129">Aboneliğinizdeki hedef depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e29f8-129">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="e29f8-130">Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="e29f8-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

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

### <span data-ttu-id="e29f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29f8-131">CommonParameters</span></span>
<span data-ttu-id="e29f8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e29f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29f8-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29f8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29f8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e29f8-134">INPUTS</span></span>

### <span data-ttu-id="e29f8-135">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e29f8-135">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint</span></span>
<span data-ttu-id="e29f8-136">Parametreler: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e29f8-136">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="e29f8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e29f8-137">OUTPUTS</span></span>

### <span data-ttu-id="e29f8-138">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="e29f8-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="e29f8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e29f8-139">NOTES</span></span>

## <span data-ttu-id="e29f8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e29f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="e29f8-141">Backup-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="e29f8-141">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="e29f8-142">Get-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="e29f8-142">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="e29f8-143">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e29f8-143">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


