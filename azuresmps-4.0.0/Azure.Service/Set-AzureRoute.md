---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105823"
---
# Set-AzureRoute

## SYNOPSIS
Yol tablosunda bir yol oluşturur.

## INDEKI

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureRoute** cmdlet 'i, yol tablosunda bir yol oluşturur.
Yeni yol, yol tablosuyla ilişkilendirilmiş sanal makinelerde hemen hemen gerçekleşir.

## ÖRNEKLERDEN

### Örnek 1: sonraki atlama rotası sanal bir gereç ekleme
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

Bu komut, belirtilen konumda ApplianceRouteTable adlı bir yol tablosu oluşturur.
Komut bu yol tablosunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, VirtualAppliance sonraki atlama türü olan ApplianceRoute03 adlı bir yol ekler.
Komut sonraki atlama IP adresini ve yolun adres önekini belirtir.

### Örnek 2: bir Internet sonraki atlama yolunu ekleme
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

Bu komut, ApplianceRouteTable adlı bir yol tablosu alır.
Komut bu yol tablosunu geçerli cmdlet 'e geçirir.
Geçerli cmdlet, ınternetroute adlı bir Internet sonraki atlama türüdür.
Komut, yolun adres önekini belirtir.

## PARAMETRELERINE

### -AddressPrefix
Yeni yol için bir adres öneki belirtir.

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

### -Nexthopıpaddress
Bu rotayı kullanan trafiğin sonraki atlaması olan gereç IP adresini belirtir.
*Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda bu değeri belirtin.

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

### -NextHopType
Bu rotayı kullanan trafik için sonraki atlama türünü belirtir.
Geçerli değerler: 

- VPNGateway
- VNETLocal
- İnternete
- VirtualAppliance
- Sonlandırılmış

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

### -RouteName
Bu cmdlet 'in eklediği yeni yolun adını belirtir.

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

### -RouteTable
Bu cmdlet 'in yeni yolu eklediği yol tablosunu belirtir.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureRoute](./Remove-AzureRoute.md)


