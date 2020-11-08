---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274180"
---
# Get-AzDataFactoryV2Pipeline

## SYNOPSIS
Veri Fabrikası içindeki ardışık düzenler hakkında bilgi alır.

## INDEKI

### ByFactoryName (varsayılan)
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Byresourceıd
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Get-AzDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'ndaki ardışık düzenler hakkında bilgi alır.
Bir ardışık düzenin adını belirtirseniz, bu cmdlet bu ardışık düzen hakkında bilgi alır.
Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm ardışık düzenler hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: tüm ardışık düzenler hakkında bilgi alma
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

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
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

### Örnek 4: ilk etkinliğin girişleri hakkında bilgi edinme
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

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
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
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
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Ad
Bilgi alınacak ardışık düzenin adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
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
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Azure Resource ID.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Set-AzDataFactoryV2Pipeline]()

[Remove-AzDataFactoryV2Pipeline]()

[Invoke-AzDataFactoryV2Pipeline]()
