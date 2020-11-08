---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106413"
---
# Set-AzureVNetGatewayDefaultSite

## SYNOPSIS
Zorunlu tünel trafiği için varsayılan siteyi ayarlar.

## INDEKI

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Set-AzureVNetGatewayDefaultSite** cmdlet 'i, Zorlamalı tünel trafiği için şirket içi sitesine varsayılan yol ayarlar.
Bu komut, bir sanal ağın Azure sanal özel ağ (VPN) ağ geçidinde yolunu ayarlar.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -Defaultsıte
Zorlamalı tünel trafiği için şirket içi yerel ağ sitesinin adını belirtir.

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
Bu cmdlet, bu parametrenin belirttiği sanal ağın Zorlamalı tünel trafiği için VPN ağ geçidinin varsayılan yolunu ayarlar.

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

[Remove-AzureVNetGatewayDefaultSite](./Remove-AzureVNetGatewayDefaultSite.md)
