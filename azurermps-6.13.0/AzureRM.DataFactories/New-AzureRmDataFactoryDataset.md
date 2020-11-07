---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 0353e1a18d881b2546bf8cc35d141ede1e87fd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764147"
---
# New-AzureRmDataFactoryDataset

## SYNOPSIS
Veri Fabrikası içinde bir veri kümesi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
New-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmDataFactoryDataset** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi oluşturur.
Zaten varolan bir veri kümesi için bir ad belirtirseniz, bu cmdlet veri kümesini değiştirmeden önce onaylamanızı ister.
*Force* parametresini belirtirseniz, cmdlet var olan veri kümesini onay olmadan değiştirir.
Bu işlemleri aşağıdaki sırada gerçekleştirin: 
- Veri Fabrikası oluşturma. 
- Bağlantılı hizmetler oluşturma. 
- Veri kümeleri oluşturma. 
- Ardışık düzen oluşturma.
Veri Fabrikası içinde aynı ada sahip bir veri kümesi varsa, bu cmdlet, var olan veri kümesinin yeni DataSet ile üzerine yazılmasını onaylamanızı ister.
Var olan veri kümesinin üzerine yazmayı onayladıktan sonra, veri kümesi tanımı da değiştirilir.

## ÖRNEKLERDEN

### Örnek 1: veri kümesi oluşturma
```
PS C:\>New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

Bu komut WikiADF adındaki DA_WikipediaClickEvents adlı veri kümesi oluşturur.
Komut, veri kümesini DAWikipediaClickEvents.jsdosyadaki bilgilerde temel alır.

### Örnek 2: yeni bir veri kümesinin uygunluk durumunu görüntüleme
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

İlk komut, önceki örnekte olduğu gibi DA_WikipediaClickEvents adlı bir veri kümesi oluşturur ve bu veri kümesini $Dataset değişkenine atar.
İkinci komut, veri kümesinin uygunluk özelliği hakkında ayrıntıları görüntülemek için standart nokta gösterimini kullanır.

### Örnek 3: yeni veri kümesinin konumunu görüntüleme
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

İlk komut, önceki örnekte olduğu gibi DA_WikipediaClickEvents adlı bir veri kümesi oluşturur ve bu veri kümesini $Dataset değişkenine atar.
İkinci komut, DataSet 'in location özelliğinin ayrıntılarını görüntüler.

### Örnek 4: yeni bir veri kümesi için geçerlilik kurallarını görüntüleme
```
PS C:\>$Dataset = New-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

İlk komut, önceki örnekte olduğu gibi DA_WikipediaClickEvents adlı bir veri kümesi oluşturur ve bu veri kümesini $Dataset değişkenine atar.
İkinci komut, DataSet 'in doğrulama kuralları hakkında ayrıntılı bilgi alır ve bunları ardışık düzen işlecini kullanarak Format-List cmdlet 'ine iletir.
Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.
Daha fazla bilgi için yazın `Get-Help Format-List` .

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.

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
Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.

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
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Dosya
Veri kümesinin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Bu cmdlet 'in varolan bir veri kümesini, sizden onay istemeden değiştirdiğini gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Oluşturulacak veri kümesinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği grupta bir veri kümesi oluşturur.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası

### System. String

## ÇıKıŞLAR

### Microsoft.Azure.Commands.DataFactories.Models.PSDatakümesi

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Get-AzureRmDataFactoryDataset](./Get-AzureRmDataFactoryDataset.md)

[Remove-AzureRmDataFactoryDataset](./Remove-AzureRmDataFactoryDataset.md)


