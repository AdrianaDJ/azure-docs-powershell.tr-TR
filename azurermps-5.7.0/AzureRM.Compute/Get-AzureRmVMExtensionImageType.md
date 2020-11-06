---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 15b1316940c42534844245eaaf1aee3e450adc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587625"
---
# Get-AzureRmVMExtensionImageType

## SYNOPSIS
Azure uzantısının türünü alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String> [<CommonParameters>]
```

## Tanım
**Get-Azurermvmextensionımagetype** cmdlet 'i, bir Azure uzantısının türünü alır.

## ÖRNEKLERDEN

### Örnek 1: uzantı resim türünü alma
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

Bu komut belirtilen yayımcının ve konumun uzantı resim türünü alır.

## PARAMETRELERINE

### -Konum
Bir uzantının konumunu belirtir.
Bu cmdlet, bu parametrenin belirttiği konumda uzantının türünü alır.

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
Bir uzantının yayıncısı adını belirtir.
Uzantı yayımcısı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.
Bu cmdlet, bu parametrenin belirttiği yayımcının türünü alır.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md)

[Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md)


