---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: b8065c3b4aa958c9138316488b7ca8a9b982d97c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594748"
---
# Get-AzureRmDataFactoryV2Pipeline

## SYNOPSIS
Veri Fabrikası içindeki ardışık düzenler hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## Tanım
Get-AzureRmDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'ndaki ardışık düzenler hakkında bilgi alır.
Bir ardışık düzenin adını belirtirseniz, bu cmdlet bu ardışık düzen hakkında bilgi alır.
Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm ardışık düzenler hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: tüm ardışık düzenler hakkında bilgi alma
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm ardışık düzenler hakkında bilgi alır.
Aşağıdaki örnek komutlardan birini kullanabilirsiniz.
İkincisi bir DataFactory nesnesini parametre olarak kullanır.

### Örnek 2: belirli bir ardışık düzen hakkında bilgi alma
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

Bu komut, WikiADF adlı veri fabrikası içinde Dpwiöörnek adlı ardışık düzen hakkında bilgi alır.
Komut bu bilgileri, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.
Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.
Daha fazla bilgi için Get-Help biçim-liste yazın.

### Örnek 3: belirli bir ardışık düzenin özelliklerini alma
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}

```

Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin etkinlikler özelliğini görüntülemek için standart nokta gösterimini kullanır.

### Örnek 6: ilk etkinliğin girişleri hakkında bilgi edinme
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :

```

Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin etkinlikler özelliğini görüntülemek için standart nokta gösterimini kullanır.
Komut, Format-List cmdlet 'ini kullanarak etkinlikler dizisinin ilk öğesinin giriş özelliğini görüntüler.

## PARAMETRELERINE

### -DataFactory
PSDataFactory nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.

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
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.

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
Bilgi alınacak ardışık düzenin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruba ait ardışık düzenleri alır.

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

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline


## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR
[Set-AzureRmDataFactoryV2Pipeline]()

[Remove-AzureRmDataFactoryV2Pipeline]()

[Invoke-AzureRmDataFactoryV2Pipeline]()
