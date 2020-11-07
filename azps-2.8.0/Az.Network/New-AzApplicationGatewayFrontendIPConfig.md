---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2ffd1d0a0ab3542636a2deec134d5bd233fd8ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918344"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Uygulama ağ geçidi için ön uç IP yapılandırması oluşturur.

## INDEKI

### Setbyresourceıd
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azapplicationgatewayfrontendıconfıg** cmdlet 'i, bir Azure Application Gateway için ön uç IP yapılandırması oluşturur.
Uygulama ağ geçidi iki tür ön uç IP yapılandırmasını destekler: 
- Genel IP adresleri--iç Yük Dengelemesi (ıLB) kullanan özel IP adresleri.
 Uygulama ağ geçidi en çok bir genel IP adresi ve bir özel IP adresi içerebilir.
Genel IP adresi ve özel IP adresi, ön uç IP adresleri olarak ayrı ayrı eklenmelidir.

## ÖRNEKLERDEN

### Örnek 1: genel IP kaynak nesnesini kullanarak ön uç IP yapılandırması oluşturma
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

İlk komut ortak IP kaynak nesnesi oluşturur ve $PublicIP değişkeninde depolar.
İkinci komut, FrontEndIP01 adlı yeni bir ön uç IP yapılandırması oluşturmak için $PublicIP kullanır ve $FrontEnd değişkeninde depolar.

### Örnek 2: ön uç IP adresi olarak statik özel bir IP oluşturma
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.
İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.
Üçüncü komut, $Subnet ikinci komuttan ve özel IP adresi 10.0.1.1 kullanarak FrontEndIP02 adlı ön uç IP yapılandırması oluşturur ve $FrontEnd değişkeninde depolar.

### Örnek 3: ön uç IP adresi olarak dinamik özel IP oluşturma
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan VNet01 adındaki bir sanal ağı alır ve $VNet değişkeninde depolar.
İkinci komut, ilk komuttan $VNet kullanarak Subnet01 adlı bir alt ağ yapılandırmasını alır ve $Subnet değişkeninde depolar.
Üçüncü komut, ikinci komuttan $Subnet kullanarak FrontEndIP03 adlı ön uç IP yapılandırması oluşturur ve bunu $FrontEnd değişkeninde depolar.

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
Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasının adını belirtir.

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

### -Privateıpaddress
Bu cmdlet 'in uygulama ağ geçidinin ön uç IP adresiyle ilişki kurduğu özel IP adresini belirtir.
Bu, yalnızca alt ağ belirtilmişse belirtilebilir.
Bu IP, alt ağdan statik olarak ayrılır.

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

### -Publicıpaddress
Bu cmdlet 'in uygulama ağ geçidinin ön uç IP adresiyle ilişki kurduğu ortak IP adresi nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publicıpadresisıd
Bu cmdlet 'in uygulama ağ geçidinin ön uç IP ile ilişki kurduğu genel IP adresi KIMLIĞINI belirtir.

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

### -Alt ağ
Bu cmdlet 'in uygulama ağ geçidinin ön uç IP adresiyle ilişki kurduğu alt ağ nesnesini belirtir.
Bu parametreyi belirtirseniz, ağ geçidinin özel bir IP adresi kullandığı anlamına gelir.
*Privateıpaddress* parametresi belirtilmişse, bu parametrenin belirttiği alt ağa ait olmalıdır.
*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.

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
Bu cmdlet 'in uygulama ağ geçidinin ön uç IP yapılandırmasıyla ilişki kurduğu alt ağ KIMLIĞINI belirtir.
*Alt ağ* parametresini belirtirseniz, ağ geçidinin özel bir IP adresi kullandığı anlamına gelir.
*Privateıpaddress* parametresi belirtilmişse *alt ağ* tarafından belirtilen alt ağa ait olmalıdır.
*Privateıpaddress* belirtilmemişse, bu alt ağdaki IP adreslerinden biri, uygulama ağ geçidinin ön uç IP adresi olarak dinamik olarak gönderilir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendIPConfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azapplicationgatewayfrontendıconfıg yapılandırması](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-Azapplicationgatewayfrontendıyapılandırma](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-Azapplicationgatewayfrontendıyapılandırma](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-Azapplicationgatewayfrontendıyapılandırma](./Set-AzApplicationGatewayFrontendIPConfig.md)


