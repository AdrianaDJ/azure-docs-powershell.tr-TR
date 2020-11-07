---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c26fe80110066e1f6305e2d35b952ed8ab45f00d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935652"
---
# Add-AzApplicationGatewayIPConfiguration

## SYNOPSIS
Uygulama ağ geçidine IP yapılandırması ekler.

## INDEKI

### Setbyresourceıd
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-Azapplicationgatewayıpconfiguration** cmdlet 'i, uygulama ağ GEÇIDINE bir IP yapılandırması ekler.
IP yapılandırmaları, uygulama ağ geçidinin dağıtıldığı alt ağı içerir.

## ÖRNEKLERDEN

### Örnek 1: uygulama ağ geçidine sanal ağ yapılandırması ekleme
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

İlk komut sanal ağ oluşturur.
İkinci komut, önceden oluşturulmuş sanal ağı kullanarak bir alt ağ oluşturur.
Üçüncü komut, uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.
Fouth komutu, IP yapılandırmasını $AppGw depolanan uygulama ağ geçidine ekler.

## PARAMETRELERINE

### -ApplicationGateway
Bu cmdlet 'in IP yapılandırması eklediği uygulama ağ geçidini belirtir.

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
Eklenecek IP yapılandırmasının adını belirtir.

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
Alt ağ belirtir.
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
Bu, uygulama ağ geçidinin dağıtıldığı alt ağdır.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azapplicationgatewayıp yapılandırması](./Get-AzApplicationGatewayIPConfiguration.md)

[Yeni-Azapplicationgatewayıp yapılandırması](./New-AzApplicationGatewayIPConfiguration.md)

[Remove-Azapplicationgatewayıp yapılandırması](./Remove-AzApplicationGatewayIPConfiguration.md)

[Set-Azapplicationgatewayıp yapılandırması](./Set-AzApplicationGatewayIPConfiguration.md)


