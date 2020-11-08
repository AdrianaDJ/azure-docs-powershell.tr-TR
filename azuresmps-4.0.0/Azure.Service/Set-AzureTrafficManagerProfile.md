---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105794"
---
# Set-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager profilinin özelliklerini güncelleştirir.

## INDEKI

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureTrafficManagerProfile** cmdlet 'ı Microsoft Azure Traffic Manager profilinin özelliklerini güncelleştirir.

*LoadBalancingMethod* değerini "yük devretme" olarak ayarlamış olduğunuz profillerde, Add-AzureTrafficManagerEndpoint cmdlet 'ine sahip profilinize eklediğiniz uç noktaların yük devretme sırasını belirleyebilirsiniz.
Daha fazla bilgi için aşağıdaki örnek 3 konusuna bakın.

## ÖRNEKLERDEN

### Örnek 1: Traffic Manager profili için TTL 'yi ayarlama
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

Bu komut, MyTrafficManagerProfile Traffic Manager profil nesnesi için TTL değerini 60 saniye olarak ayarlar.

### Örnek 2: bir profil için birkaç değer ayarlama
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Bu komut, **Get-AzureTrafficManagerProfile** cmdlet 'Ini kullanarak myprofıle adlı bir Traffic Manager profili alır.
Profil, bir Traffic Manager profili için RoundRobin Yük Dengeleme yöntemi, 30 saniye TTL, izleme Protokolü HTTP, izleyici bağlantı noktası ve göreli yol kullanır.

### Örnek 3: uç noktaları istenen yük devretme sırasına yeniden sıralama
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

Bu örnek MyProfile 'e eklenecek uç noktaları istenen yük devretme siparişine yeniden sıralar.

İlk komut Myprofıle adlı Traffic Manager profil nesnesini alır ve nesneyi $Profile değişkeninde depolar.

İkinci komut uç noktaları dizisindeki uç noktaları, yerine çalışma yerine gerçekleşecek şekilde yeniden sıralar.

Son komut $Profile uygulamasında depolanan Traffic Manager profilini yeni son nokta siparişiyle güncelleştirir.

## PARAMETRELERINE

### -LoadBalancingMethod
Bağlantıyı dağıtmak için kullanılacak yük dengeleme yöntemini belirtir.
Geçerli değerler: 

- Performans
- Devretmesini
- RoundRobin

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

### -Monitorın bağlantı noktası
Uç nokta durumunu izlemek için kullanılan bağlantı noktasını belirtir.
Geçerli değerler, 0 ' dan büyük ve 65.535 'ten küçük tamsayı değerlerdir.

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

### -MonitorProtocol
Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.
Geçerli değerler: 

- Http
- Https

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

### -MonitorRelativePath
Sistem durumu için araştırma yapılacak uç nokta etki alanı adına göre yolu belirtir.
Yol aşağıdaki kısıtlamalara uymalıdır: 

- Yol 1 ila 1000 karakter arasında olmalıdır.
- Eğik çizgiyle başlamalıdır.
- XML öğeleri içermemesi gerekir \<\> .
- Çift eğik çizgi içermemelidir,//.
- Geçersiz HTML kaçış karakterleri içermemelidir.
Örneğin,% XY.

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

### -Ad
Güncelleştirilecek Traffic Manager profilinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -TrafficManagerProfile
Profili ayarlamak için kullandığınız Traffic Manager profili nesnesini belirtir.

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

### -TTL
Yerel DNS çözümleyicilerine DNS girişlerini önbelleğe alma süresini bildiren DNS yaşam süresini (TTL) belirtir.
Geçerli değerler 30 ile 999.999 arasında bir tamsayıdır.

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
Bu cmdlet, bir Traffic Manager profil nesnesi oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


