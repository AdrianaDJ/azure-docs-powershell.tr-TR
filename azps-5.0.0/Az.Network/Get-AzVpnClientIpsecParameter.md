---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276206"
---
# Get-AzVpnClientIpsecParameter

## SYNOPSIS
Site bağlantılarının üzerine gelmek için sanal ağ geçidinde ayarlanan VPN IPSec parametrelerini alır.

## INDEKI

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.
**Get-Azvpnclientıpsecparameter** cmdlet 'ı, ağ geçidi adına ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinde ayarlanan VPN IPSec parametreleriniz nesnesini döndürür.

## ÖRNEKLERDEN

### Örnek 1: site bağlantılarının üzerine gelmek için sanal ağ geçitindeki VPN IPSec parametrelerini alır.
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

Sanal ağ geçitte "myRG" adlı sanal ağ geçidinde ayarlanan VPN IPSec parametrelerinin nesnesini döndürür

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
Kaynak adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psvpnclientıpsecparameters

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azvpnclientıpsecparameter](./New-AzVpnClientIpsecParameter.md)

[Remove-Azvpnclientıpsecparameter](./Remove-AzVpnClientIpsecParameter.md)

[Set-Azvpnclientıpsecparameter](./Set-AzVpnClientIpsecParameter.md)
