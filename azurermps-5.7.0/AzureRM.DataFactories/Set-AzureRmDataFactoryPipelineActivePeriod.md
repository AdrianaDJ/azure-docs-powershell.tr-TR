---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 1c6290f21693f599925f34f950256005df8be670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587580"
---
# Set-AzureRmDataFactoryPipelineActivePeriod

## SYNOPSIS
Veri dilimleri için etkin dönemi yapılandırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-Azurermdatafactorypelıneactivedönem** cmdlet 'ı Azure Veri Fabrikası 'nde ardışık düzen tarafından işlenen veri dilimleri için etkin dönemi yapılandırır.
Bir veri kümesindeki dilimlerin durumunu değiştirmek için Set-AzureRmDataFactorySliceStatus cmdlet 'ini kullanıyorsanız, bir dilimin başlangıç saati ve bitiş saatinin ardışık düzenin etkin döneminde olduğundan emin olun.

Bir ardışık düzen oluşturduktan sonra, veri işlemenin gerçekleştiği dönemi belirtebilirsiniz.
Potansiyel satış için etkin dönem belirtmek, veri dilimlerinin her veri fabrikası veri kümesi için tanımlanmış **kullanılabilirlik** özelliklerine bağlı olarak işlenme süresini tanımlar.

## ÖRNEKLERDEN

### Örnek 1: etkin dönemi yapılandırma
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

Bu komut, Dpıda örnek işlemler adlı ardışık düzenin etkin dönemini yapılandırır.
Komut, veri dilimlerinin başlangıç ve bitiş noktalarını değer olarak sağlar.
Komut bir $True değeri döndürür.

## PARAMETRELERINE

### -AutoResolve
Bu cmdlet 'in Otomatik Çözümle kullandığını gösterir.

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

### -DataFactory
**Psdatafactory** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait etkin dönemi değiştirir.

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
Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait etkin dönemi değiştirir.

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

### -EndDateTime
Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.
Bu dönemde veri işleme veya veri dilimleri işlenir.
**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .

*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pasifik standart saati)

Varsayılan saat dilimi göstergesi UTC.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Forcerecalbir
Bu cmdlet 'in zorla yeniden hesaplamayı kullandığını gösterir.

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

### -Ardışık Düzen adı
Ardışık düzenin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği ardışık düzenin etkin dönemini ayarlar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruba ait bir ardışık düzenin etkin dönemini değiştirir.

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

### -StartDateTime
Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.
Bu dönemde veri işleme veya veri dilimleri işlenir.

*Startdatetıme* , ISO8601 biçiminde belirtilmelidir.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Yeni-Azurermdatafactorypeline](./New-AzureRmDataFactoryPipeline.md)

[Set-AzureRmDataFactorySliceStatus](./Set-AzureRmDataFactorySliceStatus.md)


