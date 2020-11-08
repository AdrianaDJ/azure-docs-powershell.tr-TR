---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106376"
---
# Add-AzureTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager profiline uç nokta ekler.

## INDEKI

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Add-AzureTrafficManagerEndpoint** cmdlet 'ı bir Microsoft Azure Traffic Manager profiline uç nokta ekler.
Uç nokta ekledikten sonra, Pipeline işlecini kullanarak sonucu **set-AzureTrafficManagerProfile** cmdlet 'ine geçirin.
Bu cmdlet değişikliklerinizi kaydetmek için Azure 'a bağlanır.

## ÖRNEKLERDEN

### Örnek 1: profile uç nokta ekleme
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

İlk komut, ContosoProfile adlı profili almak için **Get-AzureTrafficManagerProfile** cmdlet 'ini kullanır ve ardından $TrafficManagerProfile değişkeninde depolar.

İkinci komut $TrafficManagerProfile depolanan Traffic Manager profiline bir uç nokta ekler.
Uç nokta, Contoso02App.couldapp.net etki alanı adını içerir.
Komut aynı zamanda etkinleştirilip etkinleştirilmediğini ve türünü de belirtir.
Komut, Azure 'a bağlanarak değişikliklerinizi kaydetmek için profil nesnesini **set-AzureTrafficManagerProfile** cmdlet 'ine geçirir.

### Örnek 2: belirtilen konum ve ağırlığa sahip bir uç nokta ekleme
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Bu komut bir Traffic Manager profiline uç nokta ekler.
Uç nokta, Contoso02App.couldapp.net etki alanı adını içerir.
Komut aynı zamanda etkinleştirilip etkinleştirilmediğini ve türünü de belirtir.
Komut ayrıca uç noktanın kalınlığını ve konumunu belirtir.
Bu komut, **AzureTrafficManagerProfile 'ı ayarlamak** için profil nesnesini geçirir; değişikliklerinizi kaydetmek için Azure 'a bağlanır.

## PARAMETRELERINE

### -EtkiAlanıAdı
Eklenecek uç noktanın etki alanı adını belirtir.

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
Olası değerler, konumunda listelendiği gibi, Azure bölge adlarıdır https://azure.microsoft.com/regions/ .

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Uç noktanın ekleneceği Traffic Manager profili nesnesini belirtir.

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

Required: True
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

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


