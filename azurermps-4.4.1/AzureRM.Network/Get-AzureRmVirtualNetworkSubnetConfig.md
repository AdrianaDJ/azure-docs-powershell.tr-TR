---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 494c496a9f01b41fde2df07f804f9f0c851c5f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594619"
---
# Get-AzureRmVirtualNetworkSubnetConfig

## SYNOPSIS
Sanal ağdaki bir alt ağı alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağında bir veya daha fazla alt ağ yapılandırması alır.

## ÖRNEKLERDEN

### 1: Sanal ağda alt ağ edinme
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

Bu örnek, kaynak grubunda tek alt ağı olan bir kaynak grubu ve sanal ağ oluşturur. Bu alt ağla ilgili verileri alır.

## PARAMETRELERINE

### -Ad
Bu cmdlet 'in aldığı alt ağ yapılandırmasının adını belirtir.

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

### -VirtualNetwork
Bu cmdlet 'in aldığı alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### PSVirtualNetwork
' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSSubnet

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmVirtualNetworkSubnetConfig](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[New-AzureRmVirtualNetworkSubnetConfig](./New-AzureRmVirtualNetworkSubnetConfig.md)

[Remove-AzureRmVirtualNetworkSubnetConfig](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[Set-AzureRmVirtualNetworkSubnetConfig](./Set-AzureRmVirtualNetworkSubnetConfig.md)


