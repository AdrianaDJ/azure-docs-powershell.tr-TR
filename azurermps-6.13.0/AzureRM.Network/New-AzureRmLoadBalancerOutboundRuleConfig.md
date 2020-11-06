---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: dd2c0064b92ff96fedd9e06c32b2f2f0f5a2c65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594370"
---
# New-AzureRmLoadBalancerOutboundRuleConfig

## SYNOPSIS
Bir yük dengeleyici için giden kuralı yapılandırması oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SetByResource (varsayılan)
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Setbyresourceıd
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmLoadBalancerOutboundRuleConfig** cmdlet 'i, bir Azure yük dengeleyicisi için bir giden kuralı yapılandırması oluşturur.

## ÖRNEKLERDEN

### Örnek 1: yük dengeleyici için giden kuralı oluşturma
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzureRmLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı genel bir IP adresi oluşturur ve $publicip değişkeninde depolar.
İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı ön uç IP yapılandırması oluşturur ve $frontend değişkeninde depolar.
Üçüncü komut BackendAddressPool01 adlı bir arka uç adres havuzu yapılandırması oluşturur ve $backend değişkeninde depolar.
Dördüncü komut, $frontend ve $backend ön uç ve arka uç nesnelerini kullanarak M, Boundrule adlı bir giden kuralı yapılandırması oluşturur.
*Protokol* , *Frontendıyapılandırma* ve *backendaddresspool* parametrelerinin bir giden kural yapılandırması oluşturması gerekir.

## PARAMETRELERINE

### -AllocatedOutboundPort
NAT için kullanılacak giden bağlantı noktalarının sayısı.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackendAddressPool
Bir DIP havuzuna başvuru.
Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Backendaddresspoıd
Bir DIP havuzuna başvuru.
Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Enabletcönayar
TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.
Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frontendıyapılandırma
Yük dengeleyicinin ön uç IP adresleri.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Idfaizzamansayısı
TCP boştaki bağlantının zaman aşımı

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Giden kuralının adı.

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

### -İletişim kuralı
Protokol-TCP, UDP veya tümü

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. Int32
System. String System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. model. Psresourceıd, Microsoft. Azure. Commands. Network, Version = 6.5.0.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Network. modeller. PSBackendAddressPool

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSOutboundRule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
