---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105583"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## SYNOPSIS
Bir Azure Site kurtarma planını XML biçiminde yükler.

## INDEKI

### ByRPObject (varsayılan)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Byıd
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet 'i, bir Azure Site Recovery planını XML biçiminde yükler.
Kurtarma planını güncelleştirmek ve site kurtarma sunucusuna yüklemek için bu dosyayı kullanabilirsiniz.

Kurtarma planı bir gruptaki sanal makineleri, yük devretme ve kurtarma amacıyla alır.

## ÖRNEKLERDEN

### Örnek 1: kurtarma planı dosyası alma
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Bu komut **Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'ini kullanarak kurtarma planını alır ve $RecoveryPlan değişkeninde depolar.

İkinci komut, $RecoveryPlan Site Recovery planı XML dosyasını almak için **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet 'ini kullanır.
Komut, XML dosyasını belirtilen yolda depolar.

## PARAMETRELERINE

### -ID
Alınacak kurtarma planının KIMLIĞINI belirtir.

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

### -Yol
Kurtarma planı XML dosyasının depolanacağı tam yolu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -RecoveryPlan
Kurtarma planının alınacağı bir **Asrrecoveryplan** nesnesi belirtir.
Bir **Asrrecoveryplan** nesnesi almak Için, **Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'ini kullanın.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


