---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106271"
---
# Get-AzureWebsiteMetric

## SYNOPSIS
Geçerli abonelikteki Azure Web sitesi için ölçümleri alır.

## INDEKI

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Get-AzureWebsiteMetric** cmdlet 'i geçerli abonelikteki Azure Web sitesi için ölçümleri alır.

## ÖRNEKLERDEN

### Örnek 1: Web sitesi için örnek temelinde son üç saat için ölçümleri alma
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

Bu komut, Web sitesi için en son üç saatlik ölçümleri alır.

## PARAMETRELERINE

### -EndDate
Ölçümleri almayı durdurmak için **Tarih saat**
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
Web barındırma planı iki veya daha çok bilgisayarda çalışıyorsa, bu cmdlet her bilgisayar için ölçümleri döndürür.

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
Alınacak ölçümler dizisini belirtir.
Bu parametreyi belirtmezseniz, cmdlet tüm ölçümleri alır.

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
Abonelikteki bir Web sitesinin adını belirtir.
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

### Yuvalı
Bulut hizmeti dağıtımının ortamını belirtir.
Geçerli değerler: üretim ve hazırlama.

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

### -SlotView
Bu cmdlet 'in geçerli yuvada trafiği alan ana bilgisayar adları için ölçümleri aldığını gösterir.
Zaman aralığında bir değiştirme gerçekleşirse, ölçümler birleştirilir.

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

### -StartDate
Ölçümleri almayı başlatmak için saati bir **DateTime** nesnesi olarak belirtir.

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
Ölçümler için zaman birimini belirtir.
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

###  
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla geçirebilirsiniz.

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. Utilities. WebEntities. Services. WebEntities. MetricResponse
**Get-AzureWebsiteMetric** varsayılan olarak **metricresponse** nesnelerinin dizisini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureWebsite](./Get-AzureWebsite.md)


