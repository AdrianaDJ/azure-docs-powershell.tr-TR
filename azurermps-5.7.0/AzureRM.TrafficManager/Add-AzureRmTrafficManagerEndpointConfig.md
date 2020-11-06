---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: e9e6817d9a290acf1e91067edfd90cdf8081f1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592375"
---
# Add-AzureRmTrafficManagerEndpointConfig

## SYNOPSIS
Yerel bir Traffic Manager profil nesnesine uç nokta ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Add-AzureRmTrafficManagerEndpointConfig** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine uç nokta ekler.
New-AzureRmTrafficManagerProfile veya Get-AzureRmTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.

Bu cmdlet yerel profil nesnesinde çalışır.
Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.
Uç nokta oluşturmak ve değişikliği tek bir işlemde uygulamak için New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: profile uç nokta ekleme
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.
Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.

İkinci komut, $TrafficManagerProfile depolanan profile contoso adlı bir uç nokta ekler.
Komut uç nokta yapılandırma verilerini içerir.
Bu komut yalnızca yerel nesneyi değiştirir.

Son komutu, Azure 'daki Traffic Manager profilini $TrafficManagerProfile yerel değerle eşleşecek şekilde güncelleştirir.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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

### -EndpointName
Bu cmdlet 'in eklediği Traffic Manager uç noktasının adını belirtir.

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

### -EndpointStatus
Uç noktasının durumunu belirtir.
Geçerli değerler: 

- Etkin 
- DISABLED 

Durum etkinleştirilirse, uç nokta uç durumu için araştırılan ve trafik yönlendirme yöntemine dahil edilmiştir.

```yaml
Type: String
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
Azure bölgesi adı belirtin.
Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

```yaml
Type: UInt32
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
Type: UInt32
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
Type: String
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
Yerel bir **TrafficManagerProfile** nesnesi belirtir.
Bu cmdlet bu yerel nesneyi değiştirir.
**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.

```yaml
Type: TrafficManagerProfile
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
Type: String
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
Type: UInt32
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

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Bu cmdlet değiştirilmiş bir **TrafficManagerProfile** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


