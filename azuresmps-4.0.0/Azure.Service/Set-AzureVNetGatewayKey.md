---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105810"
---
# Set-AzureVNetGatewayKey

## SYNOPSIS
Azure VPN ağ geçidi ve yerel ağ sitesi arasındaki bağlantı için önceden paylaşılan anahtarı ayarlar.

## INDEKI

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureVNetGatewayKey** cmdlet 'i Azure sanal özel ağ (VPN) ağ geçidi ile şirket içi yerel ağ sitesi arasındaki bağlantı için önceden paylaşılan anahtarı ayarlar.
Anahtar, yerel ağ sitesinin ağ geçidinde yapılandırılan anahtarla eşleşmelidir.
Anahtarlar eşleşmezse bağlantı kuramaz.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -LocalNetworkSiteName
Sanal ağ geçidine bağlanan yerel ağ sitesinin adını belirtir.

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
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -SharedKey
VPN ağ geçidine atanacak paylaşılan anahtarı belirtir.
Değer, 128 karakterden uzun olmayan alfasayısal bir dize olmalıdır.

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

### -Vağ adı
Bu cmdlet 'in bağlantı için paylaşılan anahtarı ayarladığı sanal ağı belirtir.

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

[Get-AzureVNetGatewayKey](./Get-AzureVNetGatewayKey.md)


