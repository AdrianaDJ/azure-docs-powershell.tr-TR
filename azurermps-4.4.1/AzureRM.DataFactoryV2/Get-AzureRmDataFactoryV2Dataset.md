---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594753"
---
# Get-AzureRmDataFactoryV2Dataset

## SYNOPSIS
Veri Fabrikası 'nde veri kümeleri hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## Tanım
Get-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'ndaki veri kümeleri hakkında bilgi alır.
Bir veri kümesinin adını belirtirseniz, bu cmdlet bu veri kümesi hakkında bilgi alır.
Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm veri kümeleri hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: tüm veri kümeleri hakkında bilgi alma
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm veri kümeleri hakkında bilgi alır.

### Örnek 2: belirli bir veri kümesi hakkında bilgi alma
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

Bu komut WikiADF adındaki DAWikipediaClickEvents adındaki veri kümesi hakkında bilgi alır.

## PARAMETRELERINE

### -DataFactory
PSDataFactory nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
Veri Fabrikası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.

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

### -Ad
Bilgi alınacak veri kümesinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruba ait veri kümelerini alır.

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

## GÖLGELENDIRICI

### System. String
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası


## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi


## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR
[Set-AzureRmDataFactoryV2Dataset]()

[Remove-AzureRmDataFactoryV2Dataset]()
