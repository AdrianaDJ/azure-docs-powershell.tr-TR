---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935302"
---
# Remove-AzLoadBalancerBackendAddressPoolConfig

## SYNOPSIS
Bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırır.

## INDEKI

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet 'i, bir yük dengeleyiciden bir arka uç adres havuzunu kaldırır.

## ÖRNEKLERDEN

### Örnek 1: bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırma
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

Bu komut MyLoadBalancer adlı yük dengeleyiciden alır ve BackendAddressPool02 yapılandırmasını MyLoadBalancer 'dan kaldıran **-AzLoadBalancerBackendAddressPoolConfig** öğesini kaldırır.
Son olarak, Set-AzLoadBalancer cmdlet MyLoadBalancer öğesini güncelleştirir.
Arka uç adres havuzu yapılandırmasının silebilmek için mevcut olması gerektiğini unutmayın.

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

### -LoadBalancer
Kaldırılacak arka uç adres havuzunu içeren yük dengeleyicisinin belirtir.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in kaldırıldığı arka uç adres havuzunun adını belirtir.

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

### PSLoadBalancer
' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSLoadBalancer

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzLoadBalancerBackendAddressPoolConfig](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Get-AzLoadBalancerBackendAddressPoolConfig](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[Yeni-AzLoadBalancerBackendAddressPoolConfig](./New-AzLoadBalancerBackendAddressPoolConfig.md)


