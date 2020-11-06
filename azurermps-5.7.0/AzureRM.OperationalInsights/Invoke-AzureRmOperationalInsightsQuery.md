---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: e3bfdd771413f17d4dd560a350d45fdb3f47c5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588139"
---
# Invoke-AzureRmOperationalInsightsQuery

## SYNOPSIS
Belirtilen parametrelere dayalı olarak arama sonuçlarını getirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### By
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Byworkspace nesnesi
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Invoke-Azurermoperationalınsightsquery** cmdlet 'i, arama sonuçlarını belirtilen parametrelere göre döndürür.

Döndürülen nesnenin meta veri özelliğindeki aramanın durumuna erişebilirsiniz.
Durum beklemede olduğunda, arama tamamlanmaz ve sonuçlar arşivden olacaktır.

Döndürülen nesnenin değer özelliğinden aramanın sonuçlarını alabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sorgu kullanarak arama sonuçları alma
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

Yüklendikten sonra $queryResults. sonuçlar Sorgunuzdaki tüm sonuç satırlarını içerir.

### Örnek 2: $results dönüştürün. Bir diziye
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

Bazı sorgular, çok büyük veri kümelerinin döndürülmesine neden olabilir. Bu nedenle, cmdlet 'in varsayılan davranışı bellek maliyetini azaltmak için IEnumerable döndürmelidir. Sonuç dizisi olmasını tercih ediyorsanız, IEnumerable 'yu bir diziye dönüştürmek için LINQ sıralanabilir. ToArray () genişletme yöntemini kullanabilirsiniz.

### Örnek 3: belirli bir zaman diliminde sorgu kullanarak arama sonuçları alma
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Bu sorgudaki sonuçlar son 24 saat ile sınırlanacak.

### Örnek 4: sorgu sonucuna işleme & istatistiklerini ekleme
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Oluşturma ve istatistik bilgileri hakkında bilgi için bkz.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın
```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Includerender
Belirtilmişse, metrik sorguların işleme bilgileri yanıta dahil edilir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Includestatistics
Belirtilmişse, sorgu istatistikleri yanıta dahil edilir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sorgu
Yürütülecek sorgu.

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

### -TimeSpan
Sorguyu bağlama aralığı.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekleme
Sunucunun sorguyu işlemeye harcadıkları süre için bir üst sınır koyar.
Öğrenmek https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Çalışma alanı
Çalışma alanı

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -
Çalışma alanı KIMLIĞI.

```yaml
Type: String
Parameter Sets: ByWorkspaceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace
İlk olarak, çalışma alanı KIMLIĞI PSWorkspace 'ten ayıklanır. Aksi takdirde, çalışma alanı KIMLIĞINI el ile belirtmek için alan kimliği parametresini kullanabilirsiniz.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Operationalınsights. model. PSQueryResponse
***Psqueryresponse*** sonuçları içerir, sorgu & izleyin.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

