---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 4928df8bd24769e0ebb3eb60728a30a5c55f36fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938795"
---
# New-AzureRmApplicationGatewayIPConfiguration

## SYNOPSIS
Uygulama ağ geçidi için bir IP yapılandırması oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Setbyresourceıd
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzureRmApplicationGatewayIPConfiguration** cmdlet 'i, uygulama ağ geçidi IÇIN bir IP yapılandırması oluşturur.
IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.

## ÖRNEKLERDEN

### Örnek 1: uygulama ağ geçidi için IP yapılandırması oluşturma.
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

İlk komut, VNet01 adındaki kaynak grubuna ait olan bir sanal ağı alır.

İkinci komut, önceki komutun sanal ağının ait olduğu alt ağın alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.

Üçüncü komut $Subnet kullanarak IP yapılandırmasını oluşturur.

## PARAMETRELERINE

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

### -Ad
Oluşturulacak IP yapılandırmasının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Alt ağ
Alt ağ nesnesini belirtir.
Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.

```yaml
Type: PSSubnet
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
Bu, uygulama ağ geçidinin dağıtılacağı alt ağdır.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmApplicationGatewayIPConfiguration](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[Get-AzureRmApplicationGatewayIPConfiguration](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[Remove-AzureRmApplicationGatewayIPConfiguration](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[Set-AzureRmApplicationGatewayIPConfiguration](./Set-AzureRmApplicationGatewayIPConfiguration.md)


