---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106407"
---
# Stop-AzureSiteRecoveryJob

## SYNOPSIS
Site kurtarma işini durdurur.

## INDEKI

### ByObject (varsayılan)
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Byıd
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Stop-AzureSiteRecoveryJob** cmdlet 'ı bir Azure Site Recovery işini durdurur.

## ÖRNEKLERDEN

### Örnek 1: tüm işleri durdurma
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

İlk komut **Get-AzureSiteRecoveryJob** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası Için Azure Site kurtarma işlerini alır ve sonuçları $Jobs değişkeninde depolar.

İkinci komut $Jobs tarafından belirtilen işleri durdurur.

## PARAMETRELERINE

### -ID
Durdurulacak işin KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Durdurulacak işi belirtir.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureSiteRecoveryJob](./Get-AzureSiteRecoveryJob.md)

[Restart-AzureSiteRecoveryJob](./Restart-AzureSiteRecoveryJob.md)

[Özgeçmiş-AzureSiteRecoveryJob](./Resume-AzureSiteRecoveryJob.md)


