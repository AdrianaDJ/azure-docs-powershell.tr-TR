---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a367fd8643dc29901f8dfafdbecd59a8386320a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107702"
---
# Get-AzRecoveryServicesAsrJob

## SYNOPSIS
Belirtilen ASR işinin ayrıntılarını veya kurtarma hizmetleri kasasındaki en son ASR işlerinin listesini alır.

## INDEKI

### ByParam (varsayılan)
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzRecoveryServicesAsrJob** cmdlet 'ı Azure Site Recovery işlerini alır.
Kurtarma Hizmetleri kasasındaki ASR işlerini görüntülemek için bu cmdlet 'i kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Belirli bir ASR nesnesindeki tüm işleri döndürür (çoğaltılmış öğe veya kurtarma planı gibi ASR nesnesini KIMLIĞIYLE başvuru.) 

### Örnek 2

Belirtilen ASR işinin ayrıntılarını veya kurtarma hizmetleri kasasındaki en son ASR işlerinin listesini alır. oluşturulmuş

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrJob -Job $Job
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

### -Bitişsaati
İşlerin bitiş zamanını belirtir.
Bu cmdlet belirtilen süreden önce başlatılan tüm işleri alır.
Bu parametre için bir **DateTime** nesnesi almak istiyorsanız Get-Date cmdlet 'ini kullanın.
Daha fazla bilgi için yazın `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Güncelleştirme ayrıntılarının alınacağı ASR iş nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
ASR işini ada göre belirtin.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Başlangıçsaati
İşlerin başlangıç zamanını belirtir.
Bu cmdlet belirtilen süreden sonra başlatılan tüm işleri alır.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Durumlu
ASR işinin durumunu belirtir.
Bu cmdlet belirtilen durumla eşleşen tüm işleri alır.
Bu parametre için kabul edilebilir değerler şunlardır:

- NotStarted
- Progress
- Oluşturuldu
- Diğerini
- Erişilemedi
- İptal
- Etsin

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Nesnenin KIMLIĞINI belirtir. Belirtilen nesnedeki işleri aramak için kullanılır.

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Restart-AzRecoveryServicesAsrJob](./Restart-AzRecoveryServicesAsrJob.md)

[Özgeçmiş-AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[Stop-AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
