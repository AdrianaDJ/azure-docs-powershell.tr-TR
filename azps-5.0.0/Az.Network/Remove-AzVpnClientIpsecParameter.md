---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323626"
---
# Remove-AzVpnClientIpsecParameter

## SYNOPSIS
Sanal ağ geçidi kaynağında VPN özel IPSec ilkesi kümesini kaldırır.

## INDEKI

### ByFactoryName (varsayılan)
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Byresourceıd
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.
**Remove-Azvpnclientıpsecparameter** cmdlet 'ı, sanal ağ geçidinde ayarlanan VPN özel IPSec parametrelerini kaldırır, bu da VPN ağ geçidinde varsayılan VPN IPSec Ilkesini VirtualNetworkGateway adına ve kaynak grubu adına dayalı olarak ayarlar.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ ağ geçidinde ayarlanan VPN IPSec parametrelerini siler
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

Sanal ağ geçidinde "myRG" kaynak grubunda "myGateway" adıyla ayarlanmış VPN özel IPSec parametrelerini siler. Bu komut, kaldırmanın başarılı olup olmadığını gösteren bool nesnesi döndürür.
Not: Bu, sanal ağ geçidinde varsayılan VPN IPSec ilkesini ayarlamaya çalışacaktır.

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

### -InputObject
Sanal ağ geçidi nesnesi

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Azure Resource ID.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Sanal ağ geçidi adı.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway

### System. String

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azvpnclientıpsecparameter](./Get-AzVpnClientIpsecParameter.md)

[Yeni-Azvpnclientıpsecparameter](./New-AzVpnClientIpsecParameter.md)

[Set-Azvpnclientıpsecparameter](./Set-AzVpnClientIpsecParameter.md)
