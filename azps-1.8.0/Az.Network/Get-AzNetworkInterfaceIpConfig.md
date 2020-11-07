---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 18b363abb6f96eae2a128b869d9930efdde7f41e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760542"
---
# Get-AzNetworkInterfaceIpConfig

## SYNOPSIS
Ağ arabiriminin ağ arabirimi IP yapılandırmasını alır.

## INDEKI

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabiriminden ağ arabirimi IP yapılandırmasını alır.

## ÖRNEKLERDEN

### 1: ağ arabiriminin IP yapılandırmasını alma
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

İlk komut MyNic adlı bir ağ arabirimini alır ve bunu 1 $nic değişkenine depolar. İkinci komut, bu ağ arabiriminin ipconfig1 adındaki IP yapılandırmasını alır.
    

## PARAMETRELERINE

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
Bu cmdlet 'in aldığı ağ IP yapılandırmasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterface
Bu cmdlet 'in aldığı ağ IP yapılandırmasını içeren bir **NetworkInterface** nesnesi belirtir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ

## ILGILI BAĞLANTıLAR

[Add-Aznetworkınterfaceipconfig](./Add-AzNetworkInterfaceIpConfig.md)

[New-Aznetworkınterfaceipconfig](./New-AzNetworkInterfaceIpConfig.md)

[Remove-Aznetworkınterfaceipconfig](./Remove-AzNetworkInterfaceIpConfig.md)

[Set-Aznetworkınterfaceipconfig](./Set-AzNetworkInterfaceIpConfig.md)


