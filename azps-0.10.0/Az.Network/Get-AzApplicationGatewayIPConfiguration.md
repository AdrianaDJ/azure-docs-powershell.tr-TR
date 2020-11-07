---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c7912f1a5d0539a0c81aff930cd94cb944e45bb7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935585"
---
# Get-AzApplicationGatewayIPConfiguration

## SYNOPSIS
Uygulama ağ geçidinin IP yapılandırmasını alır.

## INDEKI

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azapplicationgatewayıp** yapılandırması cmdlet 'i, bir uygulama ağ geçidinin IP yapılandırmasını alır.
IP yapılandırması, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.

## ÖRNEKLERDEN

### Örnek 1: belirli bir IP yapılandırması alma
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, $AppGw depolanan ağ geçidinden GateSubnet01 adlı bir IP yapılandırmasını alır.

### Örnek 2: IP yapılandırmalarının listesini alma
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar. İkinci komut, tüm IP yapılandırmalarının listesini alır.

## PARAMETRELERINE

### -ApplicationGateway
IP yapılandırmasını içeren uygulama ağ geçidi nesnesini belirtir.

```yaml
Type: PSApplicationGateway
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
Bu cmdlet 'in aldığı IP yapılandırmasının adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azapplicationgatewayıp yapılandırması](./Add-AzApplicationGatewayIPConfiguration.md)

[Yeni-Azapplicationgatewayıp yapılandırması](./New-AzApplicationGatewayIPConfiguration.md)

[Remove-Azapplicationgatewayıp yapılandırması](./Remove-AzApplicationGatewayIPConfiguration.md)

[Set-Azapplicationgatewayıp yapılandırması](./Set-AzApplicationGatewayIPConfiguration.md)


