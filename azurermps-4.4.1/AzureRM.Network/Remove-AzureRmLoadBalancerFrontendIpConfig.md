---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: c4809371792a2add8510b1bf7f4db39dd344b037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586896"
---
# Remove-AzureRmLoadBalancerFrontendIpConfig

## SYNOPSIS
Bir yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-Azurermloadbalancerfrontendıcaconfig** cmdlet 'i, bir Azure yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.

## ÖRNEKLERDEN

### Örnek 1: yük dengeleyiciden ön uç IP yapılandırmasını kaldırma
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

İlk komut, kaldırmak istediğiniz ön uç IP yapılandırmasıyla ilişkili yük dengeleyicın alır ve $loadbalancer değişkeninde depolar.

İkinci komut $loadbalancer ' da yük dengeleyiciden ilişkili ön uç IP yapılandırmasını kaldırır.

## PARAMETRELERINE

### -LoadBalancer
Kaldırılacak ön uç IP yapılandırmasını içeren yük dengeleyicisinin belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Kaldırılacak ön uç IP adresi yapılandırmasının adını belirtir.

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

### PSLoadBalancer
' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSLoadBalancer

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermloadbalancerfrontendıconfıg](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[Get-AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[Get-Azurermloadbalancerfrontendıconfıg](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[Yeni-Azurermloadbalancerfrontendıconfıg](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[Set-Azurermloadbalancerfrontendıconfıg](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


