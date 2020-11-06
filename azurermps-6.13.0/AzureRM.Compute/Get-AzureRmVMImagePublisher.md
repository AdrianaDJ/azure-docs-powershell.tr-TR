---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93595228"
---
# Get-AzureRmVMImagePublisher

## SYNOPSIS
VMImage yayımcılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermvmımagepublisher** cmdlet 'ı VMImage yayımcılarını alır.

## ÖRNEKLERDEN

### Örnek 1: bölge için Vmımage yayımcıları alma
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

Bu komut, Azure profilinizde Merkezi ABD bölgesi için Vmımage örneklerinin yayımcılarını alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Konum
Vmımage 'ın konumunu belirtir.

```yaml
Type: System.String
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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagepublisher

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermvmımage](./Get-AzureRmVMImage.md)

[Get-Azurermvmımageteklifini](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Save-Azurermvmımage](./Save-AzureRmVMImage.md)


