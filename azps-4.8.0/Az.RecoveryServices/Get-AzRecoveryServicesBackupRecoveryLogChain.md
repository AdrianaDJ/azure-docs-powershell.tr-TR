---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274700"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## SYNOPSIS
Bu komut, verilen yedekleme öğesinin kopuk olmayan günlük zincirinin başlangıç ve bitiş noktalarını listeler. Kullanıcının VERITABANıNA geri yüklenmesini istediğini, geçerli olup olmadığını belirlemek için bu uygulamayı kullanın.

## INDEKI

### NoFilterParameterSet (varsayılan)
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azrecoveryservicesbackuprecoverylogzincirine** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için zaman aralığı kurtarma noktalarını alır.
Bir öğe yedeklendikten sonra, bir **Azrecoveryservicesbackuprecoverylogzincirine** nesnesinin bir veya daha fazla kurtarma zamanı aralığı vardır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

İlk komut yedi günden önce tarihini alır ve $StartDate değişkeninde depolar.
İkinci komut bugünün tarihini alır ve $EndDate değişkeninde depolar.
Üçüncü komut AzureWorkload yedekleme kapsayıcılarını alır ve bunları $Container değişkeninde depolar.
Dördüncü komut yedek öğeyi alır ve ardından bunu bir yedekleme öğesi nesnesi olarak Piped cmdlet 'inde paylaşır.
Son komut $BackupItem öğesindeki öğenin kurtarma noktası zaman aralıklarının dizisini alır ve $RP değişkeninde depolar.

### Örnek 2

Bu komut, verilen yedekleme öğesinin kopuk olmayan günlük zincirinin başlangıç ve bitiş noktalarını listeler. oluşturulmuş

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -EndDate
Kurtarma noktasının getirilmesi gereken zaman aralığının bitiş zamanı

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
Kurtarma noktasının getirilmesi gereken korumalı öğe nesnesi

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

### -StartDate
Kurtarma noktasının getirilmesi gereken zaman aralığının başlangıç saati

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

### -VaultId
Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase
System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
