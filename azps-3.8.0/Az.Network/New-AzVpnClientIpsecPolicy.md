---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 8a54a0e909cd2fdfa31051c8b06f8f6414b310ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098691"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
Bu komut, kullanıcıların, VPN ağ geçidinde ayarlanan ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec ilkesi nesnesini oluşturmasına olanak tanır. Bu komut, çıkış nesnesinin hem yeni hem de mevcut ağ geçidi için VPN IPSec ilkesini ayarlamak üzere kullanılmasını sağlar.

## INDEKI

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Bu komut, kullanıcıların, VPN ağ geçidinde ayarlanan ıpsecencryption, ıpsecıntegrity, ıkeencryption, ıkeıntegrity, DhGroup gibi bir değer veya tüm değerleri belirten VPN IPSec ilkesi nesnesini oluşturmasına olanak tanır. Bu komut, çıkış nesnesinin hem yeni hem de mevcut ağ geçidi için VPN IPSec ilkesini ayarlamak üzere kullanılmasını sağlar.

## ÖRNEKLERDEN

### VPN IPSec ilkesi nesnesini tanımla:
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

Bu cmdlet, geçen bir veya tüm parametrelerin parametre değerlerini kullanarak VPN IPSec ilkesi nesnesini oluşturmak için kullanılır: Set-AzVirtualNetworkGateway _Resourcegroup: VpnClientIpsecPolicy 'in PS komut 'si New-AzVirtualNetworkGateway komut 'si:

### VPN özel IPSec ilkesini ayarlamak için yeni sanal ağ ağ geçidi oluşturma:
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Bu cmdlet, oluşturulduktan sonra sanal ağ geçidi nesnesini döndürür. 

### Mevcut sanal ağ ağ geçidinde VPN özel IPSec ilkesini ayarlama:
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

Bu cmdlet, VPN özel IPSec ilkesini ayarladıktan sonra sanal ağ geçidi nesnesini döndürür.

### VPN özel ilkesinin doğru ayarlanıp ayarlanmadıysa sanal ağ geçidi 'ni alın:
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

Bu cmdlet sanal ağ geçidi nesnesini döndürür.

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

### -Dhgrup
İlk SA için ıKE Aşama 1 ' de kullanılan VpnClient DH grupları

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ikeencryption
VpnClient ıKE şifreleme algoritması (ıKE Phase 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ikeıntegrity
VpnClient ıKE bütünlük algoritması (ıKE Phase 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipsecencryption
VpnClient IPSec şifreleme algoritması (ıKE Aşama 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipsecıntegrity
VpnClient IPSec bütünlük algoritması (ıKE Aşama 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
Yeni alt SA için ıKE Phase 2 ' de kullanılan VpnClient PFS grupları

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
KB cinsinden VpnClient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) yük boyutu

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
Saniye cinsinden VpnClient IPSec güvenlik Ilişkisi (hızlı mod veya Aşama 2 SA) ömrü

```yaml
Type: System.Int32
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

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSIpsecPolicy

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
