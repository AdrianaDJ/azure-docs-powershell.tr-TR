---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764096"
---
# New-AzureRmTrafficManagerProfile

## SYNOPSIS
Traffic Manager profili oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili oluşturur.
*Ad* parametresini ve gerekli ayarları belirtin.
Bu cmdlet, yeni profili temsil eden yerel bir nesne döndürür.

Bu cmdlet, Traffic Manager uç noktalarını yapılandırmaz.
Yerel profil nesnesini, Add-AzureRmTrafficManagerEndpointConfig cmdlet 'ini kullanarak güncelleyebilirsiniz.
Ardından Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri Traffic Manager 'a yükleyin.
Alternatif olarak, New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktalar ekleyebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: profil oluşturma
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

Bu komut, kaynak grubu ResourceGroup11 ContosoProfile adlı bir Azure Traffic Manager profili oluşturur.
DNS FQDN 'si contosoapp.trafficmanager.net.

## PARAMETRELERINE

### -CustomHeader
Yoklama istekleri için özel üstbilgi adı ve değer çiftleri listesi.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedStatusCodeRange
Yoklama istekleri için beklenen HTTP durum kodu aralıklarının listesi.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxReturn
Birden çok değerli yönlendirme yöntemiyle profillerin döndürdüğü en fazla yanıt sayısı.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Monitorıntervalınseconds
Traffic Manager 'ın Bu profildeki her uç noktanın durumunu denetlemesi gereken zaman aralığı (saniye cinsinden). Varsayılan değer 30 ' dır.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPath
Uç nokta durumunu izlemek için kullanılan yolu belirtir.
Uç nokta etki alanı adıyla ilişkili bir değer belirtin.
Bu değer eğik çizgiyle (/) başlamalıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Monitorın bağlantı noktası
Uç nokta durumunu izlemek için kullanılan TCP bağlantı noktasını belirtir.
Geçerli değerler 1 ile 65535 arasındaki tamsayılardır.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorProtocol
Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.
Geçerli değerler:

- HTTP
- HTTPS

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Monitortimeout Inseconds
Traffic Manager 'ın Bu profildeki uç noktaların sistem durumu denetimini yanıtlamasını sağlayan süre (saniye). Varsayılan 10 ' dır.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Monitortoleranda Başarısızlıksayısı
Sonraki ardışık başarısız durum denetiminin ardından, bu profildeki bir uç noktanın düşürülmeden önce, Trafik Yöneticisi toleransındaki ardışık başarısız durumu denetler. Varsayılan 3 ' dir.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in oluşturduğu Traffic Manager profili için bir ad belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileStatus
Profilin durumunu belirtir.
Geçerli değerler: etkin ve devre dışı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RelativeDnsName
Bu Traffic Manager profilinin sağladığı göreli DNS adını belirtir.
Traffic Manager bu değeri ve Azure Traffic Manager 'ın profilin tam etki alanı adını (FQDN) oluşturmak için kullandığı DNS etki alanı adını birleştirir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager profili oluşturur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri. Örneğin:

@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficRoutingMethod
Trafik yönlendirme yöntemini belirtir.
Bu yöntem, gelen DNS sorgularına yanıt olarak hangi Endpoint Traffic Manager 'ın geri döndüğü belirlenir.
Geçerli değerler:

- Performans
- Ağırlıklı
- Öncelik
- Coğrafya

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TTL
Yaşam süresi (TTL) değerini belirtir.

```yaml
Type: System.UInt32
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Bu cmdlet yeni bir TrafficManagerProfile nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Disable-AzureRmTrafficManagerProfile](./Disable-AzureRmTrafficManagerProfile.md)

[Enable-AzureRmTrafficManagerProfile](./Enable-AzureRmTrafficManagerProfile.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


