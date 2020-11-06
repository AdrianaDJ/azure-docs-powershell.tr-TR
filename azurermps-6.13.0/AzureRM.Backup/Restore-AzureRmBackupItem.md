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
# Restore-AzureRmBackupItem

## SYNOPSIS
Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Restore-Azurermbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.
Bu cmdlet, yedekleme kasasından geri yüklemeyi hesabınıza başlatır.
Geri yükleme işlemi tam sanal makineyi geri yüklemez.
Disk verilerini ve yapılandırma bilgilerini geri yükler.
Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.

## ÖRNEKLERDEN

### Örnek 1: sanal makineyi kurtarma noktasına geri yükleme
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

İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.
İkinci komut, **Get-AzureRmBackupContainer** cmdlet 'ini kullanarak $Vault kasada belirtilen ada sahip bir kapsayıcı alır.
Komut bu nesneyi $Container değişkeninde depolar.
Üçüncü komut, **Get-Azurermbackupıtem** cmdlet 'ini kullanarak $Container kapsayıcısındaki kapsayıcıda alır.
Komut bu nesneyi $BackupItem değişkeninde depolar.
Dördüncü komut $BackupItem öğenin kurtarma noktasını alır.
Komut bu nesneyi $RecoveryPoint değişkeninde depolar.
Son komutu, hedef hesap adlı hesabın kurtarma $RecoveryPoint noktasını geri yükler.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -RecoveryPoint
Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.
**Azurermbackuprecoverypoint** almak için Get-AzureRmBackupRecoveryPoint cmdlet 'ini kullanın.

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

### -StorageAccountName
Aboneliğinizdeki hedef depolama hesabının adını belirtir.
Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupRecoveryPoint
Parametreler: RecoveryPoint (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-Azurermbackupıtem](./Backup-AzureRmBackupItem.md)

[Get-Azurermbackupıtem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupRecoveryPoint](./Get-AzureRmBackupRecoveryPoint.md)


