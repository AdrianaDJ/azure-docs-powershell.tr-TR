---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 1c85bc5e2a935378630728083b19544ace8670b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936492"
---
# Set-AzVirtualNetworkGatewayVpnClientConfig

## SYNOPSIS
Sanal ağ geçidi için VPN istemcisi adres havuzunu ayarlar.

## INDEKI

### Varsayılan (varsayılan)
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Radiusserveryapılandırması
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Set-AzVirtualNetworkVpnClientConfig** cmdlet 'i sanal ağ geçidi için istemci adresi havuzunu yapılandırır.
Bu ağ geçidine bağlanan sanal özel ağ (VPN) istemcilerine, bu adres havuzundan bir IP adresi atanacaktır.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ ağ geçidine VPN istemcisi adres havuzu atama
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

Bu örnekte, ContosoVirtualGateway adlı sanal ağ geçidine VPN istemcisi adres havuzu atanır.

İlk komut ağ geçidine bir nesne başvurusu oluşturur ve nesne $Gateway adlı bir değişkende depolanır.

Örnekteki ikinci komut daha sonra, ad/16 adres havuzunu ContosoVirtualGateway 'e atamak için **set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet 'ini kullanır.

### Örnek 2: mevcut ağ geçidinde dış RADIUS tabanlı kimlik doğrulamasını yapılandırma
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

Bu örnekte, ContosoVirtualGateway adlı sanal ağ geçidine VPN istemcisi adres havuzu atanır.

İlk komut ağ geçidine bir nesne başvurusu oluşturur ve nesne $Gateway adlı bir değişkende depolanır.

Örnekteki ikinci komut daha sonra, ad/16 adres havuzunu ContosoVirtualGateway 'e atamak için **set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet 'ini kullanır. Ayrıca "TestRadiusServer" dış RADIUS sunucusunu VPN istemcileri için kimlik doğrulama için kullanılacak şekilde yapılandırır.

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

### -RadiusServerAddress
P2S dış RADIUS sunucusu adresi.

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusServerSecret
Dış RADIUS sunucusu gizliliğini P2S.

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Bu cmdlet 'in değiştirdiği VPN istemcisi yapılandırma ayarlarını içeren sanal ağ geçidi için bir nesne başvurusu belirtir.
Sanal ağ geçidi için Get-AzVirtualNetworkGateway kullanarak ve ağ geçidinin adını belirterek bir nesne başvurusu oluşturabilirsiniz.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnClientAddressPool
Bu ağ geçidine bağlanan istemcilere atanacak IP adreslerini belirtir

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.

## ÇıKıŞLAR

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)


