---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105994"
---
# New-AzureRemoteAppVNet

## SYNOPSIS
Azure RemoteApp sanal ağı oluşturur.

## INDEKI

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRemoteAppVNet** cmdlet 'ı Azure RemoteApp sanal ağı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ oluşturma
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

Bu komut, ContosoVNet adında bir sanal ağ oluşturur.

İşlemin durumunu belirlemek için, **Get-AzureRemoteAppOperationResult** cmdlet 'ini kullanarak bu cmdlet 'in DÖNDÜRDÜĞÜ izleme kimliğini kullanın.

## PARAMETRELERINE

### -Dnsserverıpaddress
DNS sunucularının IPv4 adreslerinin dizisini belirtir.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GatewayType
Kullanılacak ağ geçidi yönlendirmesinin türünü belirtir.
Bu parametre için kabul edilebilir değerler: StaticRouting veya Dynamıuting.

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LocalNetworkAddressSpace
Yerel ağ adresi alanını sınıfsız etki alanları arası yönlendirme (CıDR) gösteriminde belirten bir dizeler dizisi belirtir.
Bu adres alanı *Virtualnetworkaddressspace* parametresinin belirttiği sanal ağ adresi alanıyla çakışmamalıdır.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Konum
Sanal ağın oluşturulacağı konumu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
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

### -VirtualNetworkAddressSpace
CıDR gösteriminde sanal ağ adresi alanını belirten bir dize dizisi belirtir.
Bu, özel IP adresi aralığında olmalıdır ve *Localnetworkaddressspace* parametresinin belirttiği yerel ağ adresi alanıyla çakışamaz.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Vağ adı
Azure RemoteApp sanal ağının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Vpndeviceıpaddress
Sanal özel ağ (VPN) aygıtının adresini belirtir.
Bu, genel kullanıma açık bir adres olmalıdır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRemoteAppOperationResult](./Get-AzureRemoteAppOperationResult.md)

[Get-AzureRemoteAppVNet](./Get-AzureRemoteAppVNet.md)

[Remove-AzureRemoteAppVNet](./Remove-AzureRemoteAppVNet.md)

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


