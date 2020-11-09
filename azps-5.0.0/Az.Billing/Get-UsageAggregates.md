---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321785"
---
# Get-UsageAggregates

## SYNOPSIS
Bildirilen Azure aboneliği kullanım ayrıntılarını alır.

## INDEKI

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Usagetoplamaları** cmdlet 'i aşağıdaki özellikler tarafından toplanan Azure aboneliği kullanımı verilerini alır: 
- Kullanım rapor edildiğinde başlangıç ve bitiş saatleri.
- Günlük veya saatlik, toplama duyarlılığı.
- Aynı kaynağın birden çok örneği için örnek düzeyi ayrıntısı.
Tutarlı sonuçlar için, döndürülen veriler, kullanım ayrıntılarının Azure kaynağı tarafından raporlanma sırasında temel alınarak yapılır.
Daha fazla bilgi için bkz: Azure Faturalandırma REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c başvurusu https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) .

## ÖRNEKLERDEN

### Örnek 1: abonelik verilerini alma
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Bu komut, 5/2/2015 ile 5/5/2015 arasındaki abonelik için bildirilen kullanım verilerini alır.

## PARAMETRELERINE

### -Aggregationparçalı yapı
Verilerin toplama hassasiyetini belirtir.
Geçerli değerler: günlük ve saatlik.
Varsayılan değer günlük değeridir.

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Önceki çağrıda bulunan Yanıt gövdesinden alınan devam belirtecini belirtir.
Büyük bir sonuç kümesi için, süreklilik belirteçleri kullanılarak yanıtlar disk belleğine alınır.
Devam belirteci ilerleme için bir yer işareti görevi görür.
Bu parametreyi belirtmezseniz, veriler, *Reportedstarttime* 'te belirtilen günün başından veya saatte alınır.
Veri olan Yanıtla sayfasındaki bir sonraki bağlantıyı izlemenizi öneririz.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reportedenvseçtime
Azure Faturalandırma sistemi 'nde kaynak kullanımının ne zaman kaydedildiğini belirten rapor.
Azure, dünya genelinde birden çok veri merkezini kapsayan dağıtılmış bir sistemdir, bu nedenle Kaynağın fiili kullanım süresi olan ve kullanım olayının, kaynak kullanımı bildirilen zamanı olan faturalandırma sistemine eriştiği zaman arasında bir gecikme vardır.
Bir zaman aralığı için raporlanan bir aboneliğin tüm kullanım olaylarını almak için, bildirilen sürede sorgulama yapabilirsiniz.
Bildirilen sürede sorgulama yapsanız da cmdlet, yanıt verilerini kaynak kullanım zamanına göre toplar.
Kaynak kullanım verileri, verilerin çözümlenmesi için yararlı bir Özet.

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
Azure Faturalandırma sistemine kaynak kullanımının kaydedildiği bildirilen başlangıç zamanını belirtir.

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

### -ShowDetails
Bu cmdlet 'in kullanım verileriyle örnek düzeyi ayrıntıları verip vermediğini gösterir.
Varsayılan değer $True.
$False, hizmet, sunucu tarafında sonuçları toplar ve daha az toplam grup döndürür.
Örneğin, üç Web sitesi çalıştırıyorsanız, varsayılan olarak Web sitesi tüketimi için üç satır öğesi alırsınız.
Bununla birlikte, değer $False, aynı **SubscriptionID** , **meterId** , **usagestarttime** ve **usagebitişsaati** için tüm veriler tek satırlı bir öğeye daraltılmıştır.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commerce. Usagetoplamagetresponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
