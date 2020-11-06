---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 33deeafce23267d1b2dbc594251bc58de1914280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586745"
---
# Get-AzureRmDataFactoryActivityWindow

## SYNOPSIS
Veri Fabrikası ile ilişkilendirilmiş etkinlik pencereleri hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmDataFactoryActivityWindow** cmdlet 'i, veri fabrikası ile ilişkilendirilmiş etkinlik pencereleri hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: Veri Fabrikası ile ilişkilendirilmiş etkinlik pencerelerini alma
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

Bu komut, WikiADF adlı veri fabrikası ile ilişkili tüm etkinlik penceresi hakkında bilgi alır.

## PARAMETRELERINE

### -ActivityName
Etkinliğin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği etkinlik için etkinlik pencerelerini alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactory
Cmdlet tarafından döndürülen **Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan etkinlik pencerelerini alır.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Veri Fabrikası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan etkinlik pencerelerini alır.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
Veri kümesinin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veri kümesine ait etkinlik pencerelerini alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Filtre
Azure Arama filtresi dil bilgisi kullanılarak ifade edilen etkinlik penceresini belirtir.
Dil bilgisi hakkında bilgi için, Azure Search için OData Expression sözdiziminde https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) MSDN 'de) bakın.
Etkinlik Windows listesi, bu parametrenin belirttiği arama dizesine göre filtrelenmiş.

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

### -OrderBy
Yanıtın etkinlik penceresi liste parametrelerinden biriyle sıralı olduğunu belirtir.
Virgülle ayrılmış özelliklerin listesi.
Örneğin: WindowStart, PercentComplete.

Varsayılan olarak, düzen artan sıradır (ASC).
Listeyi azalan düzende sıralamak istiyorsanız açıklama belirtin.

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

### -Ardışık Düzen adı
Ardışık düzenin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği ardışık düzene ait etkinlik pencerelerini alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği kaynak grubuna ait etkinlik pencerelerini alır.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunEnd
Etkinlik penceresinin bitiş zamanını belirtir.
Bu cmdlet, çalışma zamanları *Runstart* ve *runend* zamanları arasında kalan etkinlik pencerelerini alır.

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

### -RunStart
Etkinlik penceresinin başlangıç saatini belirtir.
Bu cmdlet, çalışma zamanları *Runstart* ve *runend* zamanları arasında kalan etkinlik pencerelerini alır.

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

### -Üst
Bu cmdlet 'in döndürdüğü etkinlik pencerelerinin maksimum sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowEnd
Etkinlik bitiş saati penceresini belirtir.
Bu cmdlet, süresi *Windowstart* ve *windowend* Times ile biten etkinlik pencerelerini alır.

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

### -WindowStart
Etkinlik başlangıç saati penceresini belirtir.
Bu cmdlet, süresi *Windowstart* ve *windowend* Times ile biten etkinlik pencerelerini alır.

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

### -WindowState
Etkinlik penceresinin durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Yabilirsiniz
- Bekliyor
- Progress
- Çalıştırılmaya
- Erişilemedi
- Atlanan

Bu cmdlet, bu parametrenin belirttiği durumda etkinlik pencerelerini alır.

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

### -Windowsub State
Etkinlik penceresinin alt durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Edildi
- Zaman aşımına uğradı
- Doğrulama

Bu cmdlet, bu parametrenin belirttiği alt durumundaki etkinlik pencerelerini alır.

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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Windowsazve. Commands. Utilities. PSActivyWindow, Microsoft. Windowsazme. Commands. Utilities.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure Veri Fabrikası cmdlet 'Leri](./AzureRM.DataFactories.md)


