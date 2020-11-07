---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936516"
---
# Set-AzPublicIpAddress

## SYNOPSIS
Genel bir IP adresi için hedef durumunu ayarlar.

## INDEKI

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azpublicıpaddress** cmdlet 'i, genel bir IP adresinin hedef durumunu ayarlar.

## ÖRNEKLERDEN

### 1: genel IP adresinin ayırma yöntemini değiştirme
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.
İkinci komut ortak IP adresi nesnesinin ayırma yöntemini "statik" olarak ayarlar.
Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir ve tahsisat yöntemini ' statik ' olarak değiştirir. Genel bir IP adresi hemen tahsis edildi.

### 2: genel IP adresinin DNS etki alanı etiketini değiştirme
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

İlk komut, kaynak grubundaki $rgName adı $publicIPName olan genel IP adresi kaynağını alır.
İkinci komut, DomainNameLabel özelliğini gerekli DNS önekine ayarlar.
Set-AzPublicIPAddress komut ortak IP adresi kaynağını güncelleştirilmiş nesneyle güncelleştirir. DomainNameLabel & FQDN beklendiği gibi değiştirilmiştir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Pspublicıpaddress
' Publicıpaddress ' parametresi ardışık düzenin ' Pspublicıpaddress ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Pspublicıpaddress

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azpublicıpaddress](./Get-AzPublicIpAddress.md)

[New-Azpublicıpaddress](./New-AzPublicIpAddress.md)

[Remove-Azpublicıpaddress](./Remove-AzPublicIpAddress.md)


