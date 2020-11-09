---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323677"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Yeni bir VPN istemcisi iptal sertifikası oluşturur.

## INDEKI

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azvpnclientunkedcertificate** cmdlet 'i sanal ağ geçidinde kullanılmak üzere yeni bir sanal özel ağ (VPN) istemci iptal sertifikası oluşturur.
İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.
Bu cmdlet, sanal ağ geçidine atanmamış tek başına bir sertifika oluşturur.
Bunun yerine, yeni bir ağ geçidi oluştururken, **Yeni-AzvpnNew-AzVirtualNetworkGateway clientgeri** .
Örneğin, yeni bir sertifika oluşturduğunuzu ve $Certificate adlı bir değişkende depolamanızı varsayalım.
Bu sertifika nesnesini, yeni sanal ağ geçidi oluştururken kullanabilirsiniz.
Örneğin, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Daha fazla bilgi için New-AzVirtualNetworkGateway cmdlet belgelerine bakın.

## ÖRNEKLERDEN

### Örnek 1: yeni bir istemci oluşturma-iptal edilen sertifika
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Bu komut yeni bir istemci-iptal edilen sertifika oluşturur ve sertifika nesnesini $Certificate adlı bir değişkende depolar.
Bu değişken, yeni **-AzVirtualNetworkGateway** cmdlet 'i tarafından, sertifikayı yeni sanal ağ ağ geçidine eklemek için kullanılabilir.

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
Yeni istemci iptal sertifikası için benzersiz bir ad belirtir.

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

### -Parmak izi
Eklenmekte olan sertifikanın benzersiz tanımlayıcısını belirtir.
Aşağıdaki gibi bir Windows PowerShell komutunu kullanarak sertifikalarınızın parmak izi bilgilerini döndürebilirsiniz: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini döndürür.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifikası

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azvpnistemci geri alınamaz sertifikası](./Add-AzVpnClientRevokedCertificate.md)

[Get-Azvpnclientgeri alma](./Get-AzVpnClientRevokedCertificate.md)

[Remove-Azvpnclientiptal](./Remove-AzVpnClientRevokedCertificate.md)


