---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107444"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
Yerel bir Traffic Manager profil nesnesine uç nokta ekler.

## INDEKI

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzTrafficManagerEndpointConfig** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine uç nokta ekler.
New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.

Bu cmdlet yerel profil nesnesinde çalışır.
Set-AzTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.
Uç nokta oluşturmak ve değişikliği tek bir işlemde uygulamak için New-AzTrafficManagerEndpoint cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: profile uç nokta ekleme
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

İlk komut **Get-AzTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.
Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.

İkinci komut, $TrafficManagerProfile depolanan profile contoso adlı bir uç nokta ekler.
Komut uç nokta yapılandırma verilerini içerir.
Bu komut yalnızca yerel nesneyi değiştirir.

Son komutu, Azure 'daki Traffic Manager profilini $TrafficManagerProfile yerel değerle eşleşecek şekilde güncelleştirir.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
Performans trafiği yönlendirme yönteminde kullanılacak uç noktasının konumunu belirtir.
Bu parametre yalnızca ExternalEndpoints veya Nestedenvseçval türünün uç noktalarına uygulanabilir.
Performans trafiği yönlendirme yöntemi kullanıldığında bu parametreyi belirtmeniz gerekir.

Azure bölgesi adı belirtin.
Azure bölgelerinin tam listesi için bkz: Azure bölgeleri http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
Bu cmdlet 'in eklediği Traffic Manager uç noktasının adını belirtir.

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

### -EndpointStatus
Uç noktasının durumunu belirtir.
Geçerli değerler: 

- Etkin 
- DISABLED 

Durum etkinleştirilirse, uç nokta uç durumu için araştırılan ve trafik yönlendirme yöntemine dahil edilmiştir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoMapping
' Coğrafi ' trafik yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş bölgelerin listesi. Lütfen [kabul edilen değerlerin tam listesi](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)Için lütfen Traffic Manager belgelerine başvurun.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Üst profildeki Iç Içe uç noktasının kullanılabilir kabul edildiği, alt profilde kullanılması gereken en az uç nokta sayısı.
Yalnızca ' Nestedenvseçın ' türünde uç noktaya uygulanabilir.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Öncelik
Traffic Manager 'ın uç noktaya atadığı önceliği belirtir.
Bu parametre, yalnızca Traffic Manager profili öncelik için öncelik için öncelik için yapılandırılmışsa kullanılır.
Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.
Düşük değerler daha yüksek öncelikleri temsil eder.

Öncelik belirtirseniz, profildeki tüm uç noktalarda öncelikleri belirtmeniz gerekir ve iki uç nokta aynı öncelik değerini paylaşabilir.
Öncelikler belirtmezseniz, Traffic Manager uç noktalara, bir (1) başlayarak, profilin uç noktalarını listelerse, varsayılan öncelik değerlerini uç noktalara atar.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetMapping
' Alt ağ ' trafiği yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş adres aralıkları veya alt ağlar listesi.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hedef
Uç noktanın tam DNS adını belirtir.
Traffic Manager trafiği bu uç noktaya yönlendirirse DNS yanıtlarında bu değeri döndürür.
Bu parametreyi yalnızca ExternalEndpoints uç noktası türü için belirtin.
Diğer uç nokta türleri için bunun yerine *Targetresourceıd* parametresini belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Targetresourceıd
Hedefin kaynak KIMLIĞINI belirtir.
Bu parametreyi yalnızca AzureEndpoints ve Nestedenvseçpoints uç noktası türleri için belirtin.
ExternalEndpoints uç noktası türü için bunun yerine *target* parametresini belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Yerel bir **TrafficManagerProfile** nesnesi belirtir.
Bu cmdlet bu yerel nesneyi değiştirir.
**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tür
Bu cmdlet 'in Azure Traffic Manager profiline eklediği uç nokta türünü belirtir.
Geçerli değerler: 

- AzureEndpoints
- ExternalEndpoints
- Nestedenvseçpuanlar

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kalınlık
Traffic Manager 'ın uç noktaya atadığı ağırlığı belirtir.
Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.
Varsayılan değer bir (1) olur.
Bu parametre yalnızca, Traffic Manager profili ağırlıklı trafik yönlendirme yöntemiyle yapılandırılmışsa kullanılır.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile

## ÇıKıŞLAR

### Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


