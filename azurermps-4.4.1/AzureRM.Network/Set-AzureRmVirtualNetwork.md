---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594611"
---
# Set-AzureRmVirtualNetwork

## SYNOPSIS
Sanal ağın hedef durumunu ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağının hedef durumunu ayarlar.

## ÖRNEKLERDEN

### 1: sanal ağ oluşturur ve alt ağlarından birini kaldırır
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

Bu örnek, iki alt ağ içeren bir sanal ağ oluşturur. Ardından sanal ağın bellekteki gösteriminden bir alt ağ kaldırır. Ardından, hizmet tarafında değiştirilmiş sanal ağ durumunu yazmak için Set-AzureRmVirtualNetwork cmdlet 'i kullanılır.

## PARAMETRELERINE

### -VirtualNetwork
Hedef durumu temsil eden bir **VirtualNetwork** nesnesi belirtir.

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

### Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)

[New-AzureRmVirtualNetwork](./New-AzureRmVirtualNetwork.md)

[Remove-AzureRmVirtualNetwork](./Remove-AzureRmVirtualNetwork.md)


