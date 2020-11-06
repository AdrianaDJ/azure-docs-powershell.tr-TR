---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 07bfc520cfabc33ed4f72f1d0d4c46c9104a5253
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587812"
---
# New-AzureRmRedisCacheScheduleEntry

## SYNOPSIS
Zamanlama girişi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzureRmRedisCacheScheduleEntry** cmdlet 'ı **psscheduleentry** nesnesi oluşturur.
Azure Redis Cache düzeltme programı (New-AzureRmRedisCachePatchSchedule cmdlet 'i gibi) zamanlama girişi nesnelerini gerektirir.

## ÖRNEKLERDEN

### Örnek 1: hafta sonları için zamanlama girdisi oluşturma
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

Bu komut, belirtilen başlangıç zamanına ve penceresine sahip bir hafta sonu zamanlamasını temsil eden bir **Psscheduleentry** nesnesi oluşturur.

## PARAMETRELERINE

### -DayOfWeek
Zamanlama girişi için haftanın gününü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Sıradışı 
- Saatlerine 
- Den 
- Salı 
- Günü 
- Per 
- Cuma 
- Günü 
- Gününü

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaintenanceWindow
Güncelleştirmelerde izin verilen zaman penceresini belirtir.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartHourUtc
Zamanlamanın başladığı günün saatini belirtir.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Yabilirsiniz
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry
Bu cmdlet bir zamanlama girişi nesnesi döndürür.

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi

## ILGILI BAĞLANTıLAR

[Get-Azurermrediscachepatchzamanlama](./Get-AzureRmRedisCachePatchSchedule.md)

[Yeni-Azurermrediscachepatchzamanlama](./New-AzureRmRedisCachePatchSchedule.md)

[Remove-Azurermrediscachepatchzamanlama](./Remove-AzureRmRedisCachePatchSchedule.md)


