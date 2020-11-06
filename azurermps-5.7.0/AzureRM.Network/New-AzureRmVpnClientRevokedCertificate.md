---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e4b9c5e921ce9a1b46e92b40b6877beb51dc709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592940"
---
# New-AzureRmVpnClientRevokedCertificate

## SYNOPSIS
Yeni bir VPN istemcisi iptal sertifikası oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azurermvpnclientunkedcertificate** cmdlet 'i sanal ağ geçidinde kullanılmak üzere yeni bir sanal özel ağ (VPN) istemci iptal sertifikası oluşturur.
İstemci-iptal sertifikaları, istemci bilgisayarların kimlik doğrulama için belirtilen sertifikayı kullanmasını engelliyor.

Bu cmdlet, sanal ağ geçidine atanmamış tek başına bir sertifika oluşturur.
Bunun yerine, yeni bir ağ geçidi oluştururken, **Yeni-AzurermvpnNew-AzureRmVirtualNetworkGateway clientgeri**
Örneğin, yeni bir sertifika oluşturduğunuzu ve $Certificate adlı bir değişkende depolamanızı varsayalım.
Bu sertifika nesnesini, yeni sanal ağ geçidi oluştururken kullanabilirsiniz.
Örneğin,

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

Daha fazla bilgi için New-AzureRmVirtualNetworkGateway cmdlet belgelerine bakın.

## ÖRNEKLERDEN

### Örnek 1: yeni bir istemci oluşturma-iptal edilen sertifika
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Bu komut yeni bir istemci-iptal edilen sertifika oluşturur ve sertifika nesnesini $Certificate adlı bir değişkende depolar.
Bu değişken, yeni **-AzureRmVirtualNetworkGateway** cmdlet 'i tarafından, sertifikayı yeni sanal ağ ağ geçidine eklemek için kullanılabilir.

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

### -Ad
Yeni istemci iptal sertifikası için benzersiz bir ad belirtir.

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

### -Parmak izi
Eklenmekte olan sertifikanın benzersiz tanımlayıcısını belirtir.

Aşağıdaki gibi bir Windows PowerShell komutunu kullanarak sertifikalarınızın parmak izi bilgilerini döndürebilirsiniz:

`Get-ChildItem -Path Cert:\LocalMachine\Root`

Yukarıdaki komut, kök sertifika deposunda bulunan tüm yerel bilgisayar sertifikalarının bilgilerini döndürür.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

###  
Bu cmdlet, ardışık düzen girişini kabul etmez.

## ÇıKıŞLAR

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifika** nesnesinin yeni örneklerini oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermvpnclientekedcertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-Azurermvpnclientgeri alma](./Get-AzureRmVpnClientRevokedCertificate.md)

[Remove-Azurermvpnclientekedcertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


