---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 43ad564f261c423882b144d3fd9fbceba1273bcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764530"
---
# Get-AzureRmRecoveryServicesBackupRecoveryPoint

## SYNOPSIS
Yedeklenmiş öğenin kurtarma noktalarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NoFilterParameterSet (varsayılan)
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RecoveryPointId
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için kurtarma noktalarını alır.
Bir öğe yedeklendikten sonra, **Azurermrecoveryservicesbackuprecoverypoint** nesnesinin bir veya daha fazla kurtarma noktası vardır.

Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: öğenin son haftasından kurtarma noktaları alma
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

İlk komut yedi günden önce tarihini alır ve $StartDate değişkeninde depolar.

İkinci komut bugünün tarihini alır ve $EndDate değişkeninde depolar.

Üçüncü komut AzureVM yedekleme kapsayıcılarını alır ve bunları $Containers değişkeninde depolar.

Dördüncü komut V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.

Son komut, $BackupItem öğenin kurtarma noktaları dizisini alır ve $RP değişkeninde depolar.

## PARAMETRELERINE

### -EndDate
Tarih aralığının sonunu belirtir.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Öğe
Bu cmdlet 'in kurtarma noktalarını aldığı öğeyi belirtir.
**Azurermrecoveryservicesbackupıtem** nesnesi almak için Get-AzureRmRecoveryServicesBackupItem cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFileDownloadLocation
Şifrelenmiş bir sanal makinenin tuş Kasası anahtarını geri yüklemek için giriş dosyasının indirileceği konumu belirtir.

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPointId
Kurtarma noktası KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate
Tarih aralığının başlangıcını belirtir.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Itembase
Parametre ' öğe ', ardışık düzen

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase

### System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. RecoveryPointBase]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRecoveryServicesBackupContainer](./Get-AzureRmRecoveryServicesBackupContainer.md)

[Get-Azurermrecoveryservicesbackupıtem](./Get-AzureRmRecoveryServicesBackupItem.md)


