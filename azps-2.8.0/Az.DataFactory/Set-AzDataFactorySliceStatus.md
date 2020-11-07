---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: a7418dd1e0570d4e92310371e658dd130b36bc44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752456"
---
# Set-AzDataFactorySliceStatus

## SYNOPSIS
Azure Veri Fabrikası 'nde bir veri kümesi için dilimlerin durumunu ayarlar.

## INDEKI

### ByFactoryName (varsayılan)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzDataFactorySliceStatus** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesindeki dilimlerin durumunu ayarlar.

## ÖRNEKLERDEN

### Örnek 1: tüm dilimlerin durumunu ayarlama
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Bu komut, Dawikiaggregduduara adlı veri kümesindeki tüm dilimlerin, WikiADF adlı veri fabrikası beklemeyi beklemek için durumunu ayarlar.
*UpdateType* parametresinde UpstreamInPipeline değeri vardır ve bu nedenle komut veri kümesindeki her bir dilimin ve tüm bağımlı veri kümelerinin durumunu ayarlar.
Dependent veri kümeleri, potansiyel satış için giriş veri kümeleri olarak kullanılır.
Bu komut $True değerini döndürür.

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
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
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimlerin durumunu değiştirir.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
Bu cmdlet 'in dilimleri değiştirdiği veri kümesinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -EndDateTime
Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.
Bu saat, veri diliminin sonu.
**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .
*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruba ait olan dilimlerin durumunu değiştirir.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.
Bu saat, veri diliminin başlangıcıdır.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Durum
Veri dilimine atanacak bir durum belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Bekliyor.
Veri dilimi işlenmeden önce geçerlilik ilkelerine yönelik doğrulamayı beklemektedir. 
- Çalıştırılmaya.
Veri işleme tamamlandı ve veri dilimi hazır.
- Progress.
Veri işleme sürüyor. 
- Erişilemedi.
Veri işleme başarısız oldu.
- Atlanan.
Veri diliminin işlenmesi atlandı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
Dilimin güncelleştirme türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Tek tek.
Belirtilen zaman aralığındaki veri kümesindeki her bir dilimin durumunu ayarlar. 
- UpstreamInPipeline.
Veri kümesindeki her bir dilimin ve potansiyel satışın etkinlik veri kümeleri olarak kullanılan tüm bağımlı veri kümelerinin durumunu ayarlar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası

### System. String

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


