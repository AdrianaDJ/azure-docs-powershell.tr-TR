---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: bae8fb04e71700d1572b8742f8cccbb2ebe8e331
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587628"
---
# Get-AzureRmVMExtensionImage

## SYNOPSIS
Bir Azure uzantısı için tüm sürümleri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [<CommonParameters>]
```

## Tanım
**Get-Azurermvmextensionımage** cmdlet 'ı bir Azure uzantısı için tüm sürümleri alır.

## ÖRNEKLERDEN

### Örnek 1: uzantı resminin sürümlerini alma
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

Bu komut, belirtilen konum, yayıncı ve tür için uzantı resminin tüm sürümlerini alır.

## PARAMETRELERINE

### -FilterExpression
Filtre ifadesi belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Bir uzantının konumunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
Uzantı yayıncısı adını belirtir.
Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tür
Uzantının türünü belirtir.
Uzantı türü edinmek için Get-AzureRmVMExtensionImageType cmdlet 'ini kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Bu cmdlet 'in aldığı uzantının sürümünü belirtir.

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

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermvmextensionımagetype](./Get-AzureRmVMExtensionImageType.md)

[Get-Azurermvmımage](./Get-AzureRmVMImage.md)

[Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md)


