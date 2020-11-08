---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096827"
---
# Set-AzApplicationGatewayIPConfiguration

## SYNOPSIS
Uygulama ağ geçidi için bir IP yapılandırmasını değiştirir.

## INDEKI

### Setbyresourceıd
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azapplicationgatewayıp** yapılandırması cmdlet 'ı, IP yapılandırmasını değiştirir.
IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.

## ÖRNEKLERDEN

### Örnek 1: uygulama ağ geçidi için IP yapılandırmasını güncelleştirme
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki sanal ağı alır ve $VNet değişkeninde depolar.
İkinci komut $VNet kullanarak Subnet01 adındaki alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.
Üçüncü komut, ResourceGroup01 adındaki kaynak grubuna ait ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.
İleri komutu, $AppGw depolanan uygulama ağ geçidinin IP yapılandırmasını $Subnet depolanan alt ağ yapılandırmasına ayarlar.

## PARAMETRELERINE

### -ApplicationGateway
Bu cmdlet 'in bir IP yapılandırmasını ilişkilendiren bir uygulama ağ geçidi nesnesi belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
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
IP yapılandırmasının adını belirtir.

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

### -Alt ağ
Alt ağı belirtir.
Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Alt ağ KIMLIĞINI belirtir.
Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azapplicationgatewayıp yapılandırması](./Add-AzApplicationGatewayIPConfiguration.md)

[Add-Azapplicationgatewayıp yapılandırması](./Add-AzApplicationGatewayIPConfiguration.md)

[Get-Azapplicationgatewayıp yapılandırması](./Get-AzApplicationGatewayIPConfiguration.md)

[Yeni-Azapplicationgatewayıp yapılandırması](./New-AzApplicationGatewayIPConfiguration.md)

[Remove-Azapplicationgatewayıp yapılandırması](./Remove-AzApplicationGatewayIPConfiguration.md)


