---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106414"
---
# Set-AzureVNetGateway

## SYNOPSIS
Bir Azure sanal ağı için VPN ağ geçidini etkinleştirilir veya devre dışı bırakır.

## INDEKI

### Bağlan (varsayılan)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Bilgisayarla
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureVNetGateway** cmdlet 'ı, Azure sanal ağı için sanal özel ağ (VPN) ağ geçidini devre dışı bırakır veya devre dışı bırakır.
Sanal ağ geçidi sanal ağa bağlanmak için VPN uç noktasıdır.
Şirket içi yerel ağ sitesi ile sanal ağ arasındaki VPN bağlantısını etkinleştirmek veya devre dışı bırakmak için, *Bağlan* veya *Bağlantıyı kapat* parametresini belirtin.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ için sanal ağ geçidini etkinleştirme
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Bu komut, ContosoProdNet adlı Azure sanal ağı ile ContosoBranchOffice adlı yerel ağ sitesinin VPN cihazı arasındaki sanal ağ ağ geçidini etkinleştirmiştir.

### Örnek 2: sanal ağ için sanal ağ geçidini devre dışı bırakma
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Bu komut, ContosoProdNet adlı Azure sanal ağı ile ContosoBranchOffice adlı yerel ağ sitesinin VPN cihazı arasındaki sanal ağ ağ geçidini devre dışı bırakır.

## PARAMETRELERINE

### -Bağlantı
Bu cmdlet 'in sanal ağ ile yerel ağ sitesi arasındaki VPN bağlantısını etkinleştirdiğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bağlantısındaki
Bu cmdlet 'in sanal ağ ile yerel ağ sitesi arasındaki VPN bağlantısını devre dışı bırakacağını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Bu cmdlet 'in VPN bağlantısını etkinleştirmesine veya devre dışı bırakabildiği şirket içi yerel ağ sitesinin adını belirtir.

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
Bu cmdlet 'in VPN bağlantısını etkinleştirmesine veya devre dışı bırakacağını belirten sanal ağı belirtir.

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

[Resize-AzureVNetGateway](./Resize-AzureVNetGateway.md)


