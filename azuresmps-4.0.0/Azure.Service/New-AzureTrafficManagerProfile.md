---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106202"
---
# New-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager profili oluşturur.

## INDEKI

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureTrafficManagerProfile** cmdlet 'ı bir Microsoft Azure Traffic Manager profili oluşturur.

*LoadBalancingMethod* değerini "yük devretme" olarak ayarladığınız bir profili oluşturduktan sonra, Add-AzureTrafficManagerEndpoint cmdlet 'i kullanarak profilinize eklediğiniz uç noktaların yük devretme sırasını belirleyebilirsiniz.
Daha fazla bilgi için aşağıdaki örnek 2 bölümüne bakın.

## ÖRNEKLERDEN

### Örnek 1: Traffic Manager profili oluşturma
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Bu komut, belirtilen Traffic Manager etki alanında Myprofıle adlı bir Traffic Manager profili, bir deneme yük dengelemesi yöntemi, 30 saniyelik TTL, HTTP izleme protokolü, izleme bağlantı noktası 80 ve belirtilen yol ile birlikte oluşturur.

### Örnek 2: uç noktaları istenen yük devretme sırasına yeniden sıralama
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

### -EtkiAlanıAdı
Traffic Manager profilinin etki alanı adını belirtir.
Trafficmanager.net 'in alt etki alanı olmalıdır.

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

Required: True
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

Required: True
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

Required: True
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Oluşturulacak Traffic Manager profilinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -TTL
Yerel DNS çözümleyicilerine DNS girişlerini önbelleğe alma süresini bildiren DNS yaşam süresini (TTL) belirtir.
Geçerli değerler 30 ile 999.999 arasındaki tamsayılardır.

```yaml
Type: Int32
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

### Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition
Bu cmdlet, bir Traffic Manager profil nesnesi oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


