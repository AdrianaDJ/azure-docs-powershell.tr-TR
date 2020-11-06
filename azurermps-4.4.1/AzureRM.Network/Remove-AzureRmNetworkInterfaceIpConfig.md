---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8afc90c8709869a9acf3464c4ad39bdbc2b3ab5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586884"
---
# Remove-AzureRmNetworkInterfaceIpConfig

## SYNOPSIS
Ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-Azurermnetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını kaldırır.

## ÖRNEKLERDEN

### 1: ağ arabiriminden IP yapılandırmasını silme
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

İlk komut MyNic adlı bir ağ arabirimi alır ve bunu $nic değişkende depolar. İkinci komut, bu ağ arabirimiyle ilişkili Ipconfig-1 adlı IP yapılandırmasını kaldırır.

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

### -Ad
Kaldırılacak ağ arabirimi IP yapılandırmasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterface
Bir **NetworkInterface** nesnesi belirtir.
Bu nesne, kaldırılacak ağ arabirimi IP yapılandırmasını içerir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
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

### Psnetworkınterface
Parametre ' NetworkInterface ', ardışık düzen

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ

## ILGILI BAĞLANTıLAR

[Add-Azurermnetworkınterfaceipconfig](./Add-AzureRmNetworkInterfaceIpConfig.md)

[Get-Azurermnetworkınterfaceipconfig](./Get-AzureRmNetworkInterfaceIpConfig.md)

[Yeni-Azurermnetworkınterfaceipconfig](./New-AzureRmNetworkInterfaceIpConfig.md)

[Set-Azurermnetworkınterfaceipconfig](./Set-AzureRmNetworkInterfaceIpConfig.md)


