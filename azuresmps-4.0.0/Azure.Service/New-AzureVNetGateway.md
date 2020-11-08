---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106187"
---
# New-AzureVNetGateway

## SYNOPSIS
Sanal ağda VPN ağ geçidi oluşturur.

## INDEKI

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureVNetGateway** cmdlet 'i sanal bir ağda sanal özel ağ (VPN) ağ geçidi oluşturur.
Ayrıca, ağ geçidi SKU 'yu varsayılan, standart veya HighPerformance olarak da belirtebilirsiniz.
Türü (StaticRouting veya Dynamıuting) belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ geçidi oluşturma
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

Bu komut, ContosoVN07 adındaki sanal ağda sanal ağ geçidi oluşturur.
Ağ Geçidi varsayılan SKU.

## PARAMETRELERINE

### -GatewaySKU
Bu cmdlet 'in oluşturduğu sanal ağ geçidinin SKU adını belirtir.
Geçerli değerler: 

- Varsayýlan 
- Ardından 
- Üst performans

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewayType
Bu cmdlet 'in oluşturduğu ağ geçidi türünü belirtir.
Geçerli değerler: 

- StaticRouting 
- Dynamikrokapatma

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
Bu cmdlet 'in sanal ağ geçidi eklediği sanal ağı belirtir.

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

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Resize-AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


