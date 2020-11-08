---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105434"
---
# Set-AzureTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager profilindeki uç noktasının özelliklerini güncelleştirir.

## INDEKI

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureTrafficManagerEndpoint** cmdlet 'ı, Microsoft Azure Traffic Manager profilinde uç noktanın özelliklerini güncelleştirir.
Uç nokta geçerli profilde yoksa, bu cmdlet bunu oluşturur.
Uç nokta ekledikten sonra, Pipeline işlecini kullanarak sonucu **set-AzureTrafficManagerProfile** cmdlet 'ine geçirin.
Bu cmdlet değişikliklerinizi kaydetmek için Azure 'a bağlanır.

## ÖRNEKLERDEN

### Örnek 1: bir profilin uç noktasını güncelleştirme
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

İlk komut, ContosoProfile adlı profili almak için **Get-AzureTrafficManagerProfile** cmdlet 'ini kullanır ve ardından $TrafficManagerProfile değişkeninde depolar.

İkinci komut $TrafficManagerProfile depolanan Traffic Manager profilindeki uç noktayı güncelleştirir.
Uç nokta, ContosoApp02.cloudapp.net etki alanı adını içerir.
Komut ayrıca uç noktanın durumunu, türünü, ağırlığını ve konumunu da belirtir.
Bu komut, değişiklikleri kaydetmek üzere Azure 'a bağlanmak için değiştirilmiş profili **set-AzureTrafficManagerProfile** cmdlet 'ine geçirir.

## PARAMETRELERINE

### -EtkiAlanıAdı
Değiştirilecek uç noktanın etki alanı adını belirtir.

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

### -Konum
Cmdlet 'in eklediği uç noktasının konumunu belirtir.
Bu bir Azure konumu olmalıdır.

Bu parametre "Any" türünde veya "TrafficManager" türünde, yük dengeleme yönteminin "performans" olarak ayarlandığı bir profildeki uç noktalar için değer içermelidir.
Olası değerler, konumunda listelendiği gibi, Azure bölge adlarıdır  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .

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

### -MinChildEndpoints
İç içe profilin bu uç nokta için çevrimiçi olması gereken en az uç nokta sayısını belirtir.

```yaml
Type: Int32
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

### -Durum
İzleme uç noktasının durumunu belirtir.
Geçerli değerler: 

- Etkin
- DISABLED

Etkin bir değer belirtirseniz, Traffic Manager uç noktayı izler ve yük dengeleme yöntemi trafiği yönetirken dikkate alır.

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

### -TrafficManagerProfile
Uç noktanın değiştirileceği Traffic Manager profili nesnesini belirtir.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Tür
Uç nokta türünü belirtir.
Geçerli değerler: 

- CloudService
- AzureWebsite
- TrafficManager

- Tüm 

Birden çok AzureWebsite uç noktası varsa uç noktalar farklı datacenters 'da olmalıdır.

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

### -Kalınlık
Cmdlet 'in eklediği uç noktanın kalınlığını belirtir.
Bu parametre için geçerli değer aralığı \[ 1, 1000 ' dir \] .

Bu parametre yalnızca RoundRobin Yük Dengeleme ilkeleri için kullanılır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition
Bu cmdlet, güncelleştirilmiş profil hakkında bilgi içeren bir Traffic Manager profili nesnesi oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


