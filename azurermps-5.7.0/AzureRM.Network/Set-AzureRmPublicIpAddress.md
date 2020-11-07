---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: df1c03551d520a833e8b974ae2a2b71fe442c4c4
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765212"
---
# Set-AzureRmPublicIpAddress

## SYNOPSIS
Genel bir IP adresi için hedef durumunu ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azurermpublicıpaddress** cmdlet 'ı ortak IP adresi için hedef durumunu ayarlar.

## ÖRNEKLERDEN

### 1: genel IP adresinin ayırma yöntemini değiştirme
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.
İkinci komut ortak IP adresi nesnesinin ayırma yöntemini "statik" olarak ayarlar.
Set-AzureRmPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir ve tahsisat yöntemini ' statik ' olarak değiştirir. Genel bir IP adresi hemen tahsis edildi.

### 2: genel IP adresinin DNS etki alanı etiketini değiştirme
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.
İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.
Set-AzureRmPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir. DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Publicıpaddress
Genel IP adresinin ayarlanması gereken hedef durumu temsil eden **Publicıpaddress** nesnesini belirtir.

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Pspublicıpaddress
' Publicıpaddress ' parametresi ardışık düzenin ' Pspublicıpaddress ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Pspublicıpaddress

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermpublicıpaddress](./Get-AzureRmPublicIpAddress.md)

[Yeni-Azurermpublicıpaddress](./New-AzureRmPublicIpAddress.md)

[Remove-Azurermpublicıpaddress](./Remove-AzureRmPublicIpAddress.md)


