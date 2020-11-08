---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105489"
---
# Remove-AzureVNetGatewayDefaultSite

## SYNOPSIS
Zorunlu tünel trafiğinin varsayılan yolunu kaldırır.

## INDEKI

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Remove-AzureVNetGatewayDefaultSite** cmdlet 'i, Zorlamalı tünel trafiği için şirket içi sitesinin varsayılan yolunu kaldırır.
Bu cmdlet, bir sanal ağın Azure sanal özel ağ (VPN) ağ geçidinden yolunu kaldırır.

## ÖRNEKLERDEN

### Örnek 1: varsayılan siteye bir yol kaldırma
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

Bu komut, ContosoVNet01 adındaki sanal ağın VPN 'sinden varsayılan site yolunu kaldırır.

## PARAMETRELERINE

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vağ adı
Sanal ağ belirtir.
Bu cmdlet, bu parametrenin belirttiği sanal ağın VPN ağ geçidinden varsayılan yolunu kaldırır.

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

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureVNetGatewayDefaultSite](./Set-AzureVNetGatewayDefaultSite.md)
