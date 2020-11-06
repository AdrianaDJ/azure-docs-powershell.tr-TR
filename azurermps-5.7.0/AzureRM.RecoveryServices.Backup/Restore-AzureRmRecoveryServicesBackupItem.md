---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 6013531367f5996924da1776c0062ebb5ad02b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587484"
---
# Restore-AzureRmRecoveryServicesBackupItem

## SYNOPSIS
Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Restore-Azurermrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.
Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.

Geri yükleme işlemi tam sanal makineyi geri yüklemez.
Disk verilerini ve yapılandırma bilgilerini geri yükler.
Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.

Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: öğeyi kurtarma noktasına geri yükleme
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

İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.

İkinci komut, V2VM adındaki yedekleme öğesini $Container alır ve $BackupItem değişkeninde depolar.

Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.

Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.

Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.
Belirtilen tarih aralığı son 7 gündür.

Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -RecoveryPoint
Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.
**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet 'ini kullanın.

```yaml
Type: RecoveryPointBase
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName
Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.
Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount
Kurtarma noktasındaki disklerin orijinal depolama hesaplarına geri yüklenebilmesi durumunda bu anahtarı kullanın.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

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

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### RecoveryPointBase
' RecoveryPoint ' parametresi ardışık düzenin ' RecoveryPointBase ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-Azurermrecoveryservicesbackupıtem](./Backup-AzureRmRecoveryServicesBackupItem.md)

[Get-Azurermrecoveryservicesbackupıtem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupRecoveryPoint](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


