---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106510"
---
# Get-AzureWebHostingPlanMetric

## SYNOPSIS
Azure Web sitesi barındırma planları için ölçümleri alır.

## INDEKI

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Get-AzureWebHostingPlanMetric** cmdlet 'i, bir abonelikteki Azure Web barındırma planları için ölçümleri alır.

## ÖRNEKLERDEN

### Örnek 1: örnek başına son üç saat için ölçümleri alma
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

Bu komut, örnek düzeyindeki son üç saat için Web barındırma planı ölçümlerini alır.

## PARAMETRELERINE

### -EndDate
Bitiş saatini, ölçü iade edilecek bir **DateTime** nesnesi olarak belirtir.
**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.
Daha fazla bilgi için yazın `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Instancedetails
Bu cmdlet 'in ayrıntıları örnek başına olarak içerdiğini gösterir.
Web sitesi barındırma planı iki veya daha fazla makinede çalışıyorsa, bu cmdlet her bir makinenin Ayrıntılar ölçülerini döndürür.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Metrik adları
Türleri.
Bu parametre için bir değer belirtmezseniz, bu cmdlet tüm ölçümleri alır.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Abonelikteki bir planın adını belirtir.
**Get-AzureWebHostingPlanMetric** , varsayılan olarak geçerli abonelikteki tüm Web sitelerini alır.
Bu parametre joker karakterleri desteklemez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -StartDate
Başlangıç zamanını, ölçümlerin alınacağı bir **DateTime** nesnesi olarak belirtir.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zaman çizgisi
Ölçümlerin alınacağı zaman birimini belirtir.
Geçerli değerler: 

- PT1M (dakika) 
- PT1H (saat) 
- P1D (gün)

Varsayılan değer PT1H ' dır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebSpaceName
Abonelikteki bir Web sayfasının adını belirtir.
Varsayılan olarak **Get-AzureWebHostingPlanMetric** , geçerli abonelikteki tüm planları alır.
Bu parametre joker karakterleri desteklemez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

###  
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla geçirebilirsiniz.

## ÇıKıŞLAR

###  
Microsoft. Windowsazve. Commands. Utilities. WebEntities. Services. WebEntities. MetricResponse

**Get-AzureWebHostingPlanMetric** varsayılan olarak **metricresponse** nesnelerinin dizisini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureWebHostingPlan](./Get-AzureWebHostingPlan.md)


