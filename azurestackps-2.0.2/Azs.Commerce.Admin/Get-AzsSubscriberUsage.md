---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106958"
---
# Get-AzsSubscriberUsage

## SYNOPSIS
Kullanıcılardan gelen Usage toplamları olan SubscriberUsageAggregates koleksiyonunu alır.

## INDEKI

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Tanım
Kullanıcılardan gelen Usage toplamları olan SubscriberUsageAggregates koleksiyonunu alır.

## ÖRNEKLERDEN

### Örnek 1: güne göre toplanan kullanım verilerini al
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

Gün tarafından toplanan tüm kiracıları için 30 Ara 2019 (UTC olarak) tüm gününün kullanım verilerini alın.
ReportedStartTime ve Reportedenvseçtime, günlere yuvarlanmalıdır.
Hizmet Yöneticisi olarak çağrılırsa, bu işlem tüm kiracının tüm kullanım verilerini gösterir.

### Örnek 2: saatte toplanan kullanım verilerini alma
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

Saat esasına göre toplanmış 30 TL 'nin 2019 (UTC)
ReportedStartTime ve Reportedenvseçtime saate yuvarlanmalıdır.
Aynı şekilde, hizmet yöneticisi olarak çağrılırsa, bu işlem tüm kiracının tüm kullanım verilerini gösterir.

## PARAMETRELERINE

### -Aggregationparçalı yapı
Toplama ayrıntı düzeyi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ContinuationToken
Devam belirteci.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Reportedenvseçtime
Bildirilen bitiş zamanı (özel).

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ReportedStartTime
Bildirilen başlangıç zamanı (dahil).

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriberId
Kiracı aboneliği tanıtıcısı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. Commerce. modeller. Api20150601Preview. ıusageaggregate



## NOTLARıNDA

## ILGILI BAĞLANTıLAR

