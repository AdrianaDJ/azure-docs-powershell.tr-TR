---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106087"
---
# Resize-AzureVNetGateway

## SYNOPSIS
VPN ağ geçidini yeniden boyutlandırır.

## INDEKI

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Resize-AzureVNetGateway** cmdlet 'i sanal ağ sanal özel ağ (VPN) ağ geçidini farklı bir SKU 'ya yeniden boyutlandırır.
Sanal ağ geçidi için geçerli SKU 'Lar varsayılan, standart ve HighPerformance.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ geçidi için SKU 'YU değiştirme
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

Bu komut, ContosoVN07 adındaki sanal ağın sanal ağ geçidinin SKU 'SU

## PARAMETRELERINE

### -GatewaySKU
Bu cmdlet 'in sanal ağ geçidini yeniden boyutlandırdıkları SKU 'YU belirtir.
Geçerli değerler: 

- Varsayýlan 
- Ardından 
- Üst performans

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

### -Vağ adı
Bu cmdlet 'in sanal ağ ağ geçidini yeniden boyutlandırdıkları sanal ağı belirtir.

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

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[New-AzureVNetGateway](./New-AzureVNetGateway.md)

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Set-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


