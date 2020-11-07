---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9e15979b7e54ef926e7b4355a70568f39594112f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932768"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager profilinde uç nokta oluşturur.

## INDEKI

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profilinde uç nokta oluşturur.

Bu cmdlet, her yeni uç noktayı Traffic Manager hizmetine kaydeder.
Yerel bir Traffic Manager profil nesnesine birden çok uç nokta eklemek ve değişiklikleri tek bir işlemde uygulamak için Add-AzTrafficManagerEndpointConfig cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: bir profil için dış uç nokta oluşturma
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Bu komut, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profildeki contoso adlı bir dış uç nokta oluşturur.

### Örnek 2: bir profil için Azure uç noktası oluşturma
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Bu komut, kaynak grup ResourceGroup11 ' nde ContosoProfile adlı profildeki contoso adlı bir Azure uç noktası oluşturur.
Azure Endpoint, Azure Resource Manager KIMLIĞI 'nin *Targetresourceıd* içindeki URI yolundan verildiği Azure Web App 'e işaret ediyor.
Web App kaynağı bu konumu sağladığı için, komut, *Endpointlocation* parametresini belirtmez.

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
Bu parametre yalnızca ExternalEndpoints veya Nestedenvseçpoints türünün uç noktalarına uygulanabilir.
Performans trafiği yönlendirme yöntemi kullanıldığında bu parametreyi belirtmeniz gerekir.

Azure bölgesi adı belirtin.
Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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
' Coğrafi ' trafik yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş bölgelerin listesi. Lütfen kabul edilen değerlerin tam listesi için lütfen Traffic Manager belgelerine başvurun.

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
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in oluşturduğu Traffic Manager uç noktasının adını belirtir.

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

### -ProfileName
Bu cmdlet 'in uç nokta eklediği bir Traffic Manager profilinin adını belirtir.
Profil edinmek için New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanın.

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
Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager uç noktası oluşturur.

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

### -Tür
Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


