---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760682"
---
# Add-AzVirtualNetworkSubnetConfig

## SYNOPSIS
Sanal ağa alt ağ yapılandırması ekler.

## INDEKI

### SetByResource (varsayılan)
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Setbyresourceıd
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzVirtualNetworkSubnetConfig** cmdlet 'i mevcut bir Azure sanal ağına alt ağ yapılandırması ekler.

## ÖRNEKLERDEN

### 1: var olan bir sanal ağa alt ağ ekleme
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  Bu örnek ilk olarak, oluşturulacak kaynakların kapsayıcısı olarak bir kaynak grubu oluşturur. Ardından bir alt ağ yapılandırması oluşturur ve sanal bir ağ oluşturmak için bu yapılandırmayı kullanır. Ardından Add-AzVirtualNetworkSubnetConfig sanal ağın bellekteki gösterimine alt ağ eklemek için kullanılır. Set-AzVirtualNetwork komutu, varolan sanal ağı yeni alt ağla güncelleştirir.

### 2: var olan sanal ağa eklenen bir alt ağa temsilci ekleme
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

Bu örnek ilk olarak mevcut bir VNET alır.
Ardından bellekte bir temsilci nesnesi oluşturur.
Son olarak, bu temsilciyle VNET 'e eklenen yeni bir alt ağ oluşturur. Değiştirilen yapılandırma sunucuya gönderilir.

## PARAMETRELERINE

### -AddressPrefix
Alt ağ yapılandırması için IP adresi aralığını belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Temsilci
Bu alt ağda işlemleri gerçekleştirme izni olan hizmetlerin listesi.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Eklenecek alt ağ yapılandırmasının adını belirtir.

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

### -NetworkSecurityGroup
Bir **Networksecuritygroup** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği nesneye sanal ağ alt ağı yapılandırması ekler.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Networksecuritygroupıd
Ağ güvenlik grubunun KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteTable
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Routetableıd
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
Hizmet uç noktası değeri

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpointPolicy
Hizmet uç noktası Ilkeleri

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Alt ağ yapılandırmasının ekleneceği **VirtualNetwork** nesnesini belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork

### System. String

### Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup

### Microsoft. Azure. Commands. Network. modeller. PSRouteTable

### System. String []

### Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy []

### Microsoft.Azure.Commands.Network.Models.PSD.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)

[New-AzVirtualNetworkSubnetConfig](./New-AzVirtualNetworkSubnetConfig.md)

[Remove-AzVirtualNetworkSubnetConfig](./Remove-AzVirtualNetworkSubnetConfig.md)

[Set-AzVirtualNetworkSubnetConfig](./Set-AzVirtualNetworkSubnetConfig.md)
