---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: 6583da48324078d321630f23097ab3a00d8338d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752498"
---
# New-AzDataFactoryPipeline

## SYNOPSIS
Veri Fabrikası içinde bir ardışık düzen oluşturur.

## INDEKI

### ByFactoryName (varsayılan)
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-Azverfactorypypeline** cmdlet, Azure Veri Fabrikası 'nde bir ardışık düzen oluşturur.
Önceden var olan bir ardışık düzen için ad belirtirseniz, cmdlet, ardışık düzeni değiştirmeden önce sizden onay sorar.
*Force* parametresini belirtirseniz, cmdlet mevcut ardışık düzenin yerine geçer.
Bu işlemleri aşağıdaki sırada gerçekleştirin: 
- Veri Fabrikası oluşturma. 
- Bağlantılı hizmetler oluşturma. 
- Veri kümeleri oluşturma. 
- Ardışık düzen oluşturma.
Veri Fabrikası içinde aynı ada sahip bir ardışık düzen varsa, bu cmdlet yeni ardışık düzenin mevcut ardışık düzenin üzerine yazılıp yazılmayacağını onaylamanızı ister.
Mevcut ardışık düzenin üzerine yazılmasını onaylamıyorsanız, ardışık düzen tanımı da değiştirilir.

## ÖRNEKLERDEN

### Örnek 1: ardışık düzen oluşturma
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

Bu komut, ADF adlı veri fabrikası içinde Dpwiöörnek adlı bir ardışık düzen oluşturur.
Komut, ardışık düzeni DPWikisample.jsdosyadaki bilgileri temel alır.
Bu dosya, ardışık düzene kopyalama etkinliği ve HDInsight etkinliği gibi etkinlikler hakkında bilgi içerir.

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.

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
Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dosya
Ardışık düzenin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.

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
Bu cmdlet 'in mevcut bir ardışık düzeni sizden onay istemeden değiştirdiğini gösterir.

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
Oluşturulacak ardışık düzenin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği grup için bir ardışık düzen oluşturur.

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

### System. String

### Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataFactory. modeller. PSPipeline

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Get-Azverfactorypya](./Get-AzDataFactoryPipeline.md)

[Remove-Azdatafactorypda](./Remove-AzDataFactoryPipeline.md)

[Özgeçmiş-Azverfactorypya](./Resume-AzDataFactoryPipeline.md)

[Set-Azdatafactorypipelineactivedönem](./Set-AzDataFactoryPipelineActivePeriod.md)

[Askıya al-Azverfactorypya](./Suspend-AzDataFactoryPipeline.md)


