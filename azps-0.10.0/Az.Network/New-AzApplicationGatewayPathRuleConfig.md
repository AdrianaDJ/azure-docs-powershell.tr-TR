---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935427"
---
# New-AzApplicationGatewayPathRuleConfig

## SYNOPSIS
Uygulama ağ geçidi yol kuralı oluşturur.

## INDEKI

### Setbyresourceıd
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-AzApplicationGatewayPathRuleConfig** cmdlet 'i bir uygulama ağ geçidi yolu kuralı oluşturur.
Bu cmdlet tarafından oluşturulan kurallar URL yol haritası yapılandırma ayarları koleksiyonuna eklenebilir ve ardından bir ağ geçidine atanabilir.

Yol haritası yapılandırma ayarları uygulama ağ geçidi yük dengelemesi 'nde kullanılır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Bu komutlar yeni bir uygulama ağ geçidi yol kuralı oluşturur ve ardından bu kuralı uygulama ağ geçidine atamak için **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet 'ini kullanır.
Bunu yapmak için ilk komut ağ geçidi ContosoApplicationGateway 'e bir nesne başvurusu oluşturur.
Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.

Sonraki iki komut arka uç adres havuzu ve arka uç HTTP Ayarları nesnesi oluşturur; yol kuralı nesnesi oluşturmak için bu nesneler ($AddressPool ve $HttpSettings 'te depolanan) gereklidir.

Dördüncü komut, yol kuralı nesnesini oluşturur ve $PathRuleConfig adlı bir değişkende saklanır.

Beşinci komut, yapılandırma ayarlarını ve bu ayarlarda bulunan yeni yol kuralını ContosoApplicationGateway 'e eklemek için **Add-AzApplicationGatewayUrlPathMapConfig** öğesini kullanır.

## PARAMETRELERINE

### -BackendAddressPool
Ağ Geçidi yol kuralları yapılandırma ayarlarına eklenecek bir arka uç adres havuzu ayarları koleksiyonuna bir nesne başvurusu belirtir.
Bu nesne başvurusunu, New-AzApplicationGatewayBackendAddressPool cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz:

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

Yukarıdaki komut, adres havuzuna iki IP adresi (192.16.1.1 ve 192.168.1.2) ekler.
IP adresinin tırnak işaretleri içine alındığına ve virgül kullanılarak ayrıldığına dikkat edin.

Sonuç değişkeni $AddressPool, *Defaultbackendaddresspool* parametresinin parametre değeri olarak kullanılabilir.

Arka uç adres havuzu, arka uç sunucularındaki IP adreslerini temsil eder.
Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.
Bu parametreyi kullanırsanız, *Defaultbackendaddresspoıd* parametresini aynı komutta kullanamazsınız.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Backendaddresspoıd
Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç adres havuzunun KIMLIĞINI belirtir.
Adres havuzu kimlikleri Get-AzApplicationGatewayBackendAddressPool cmdlet kullanılarak döndürülebilir.
KIMLIĞI aldıktan sonra *defaultbackendaddresspool* parametresi yerine *Defaultbackendaddresspoıd* parametresini kullanabilirsiniz.
Örneğin:

-Defaultbackendaddresspoıd "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

Arka uç adres havuzu, arka uç sunucularındaki IP adreslerini temsil eder.
Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenecek bir arka uç HTTP ayarları koleksiyonuna bir nesne başvurusu belirtir.
Bu nesne başvurusunu, New-AzApplicationGatewayBackendHttpSetting cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz:

$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-Name "Contosohttpsetler"-port 80-Protocol "http"-Bina ıebasedaffinity "Disabled"

Sonuç değişkeni $HttpSettings, *Defaultbackendaddresspool* parametresinin parametre değeri olarak kullanılabilir:

-DefaultBackendHttpSettings $HttpSettings

Arka uç HTTP ayarları, bir arka uç havuzunun bağlantı noktası, protokolü ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırır.
Bu parametreyi kullanırsanız, *Defaultbackendhttpsettingsid* parametresini aynı komutta kullanamazsınız.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç HTTP ayarları koleksiyonunun KIMLIĞINI belirtir.
HTTP ayar kimlikleri, Get-AzApplicationGatewayBackendHttpSetting cmdlet kullanılarak döndürülebilir.
KIMLIĞI aldıktan sonra, *Defaultbackendhttpsettings* parametresi yerine *Defaultbackendhttpsettingsıd* parametresini kullanabilirsiniz.
Örneğin:

-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

Arka uç HTTP ayarları, bir arka uç havuzunun bağlantı noktası, protokolü ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırır.
Bu parametreyi kullanırsanız, *Defaultbackendhttpsettings* parametresini aynı komutta kullanamazsınız.

```yaml
Type: String
Parameter Sets: SetByResourceId
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in oluşturduğu yol kuralı yapılandırmasının adını belirtir.

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

### -Yollar
Bir veya daha fazla uygulama ağ geçidi yol kuralını belirtir.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
Uygulama ağ geçidi Redirectyapılandırması

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Redirectconfigurationıd
Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI

```yaml
Type: String
Parameter Sets: SetByResourceId
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

###  
**New-AzApplicationGatewayPathRuleConfig** , ardışık düzen girişini kabul etmez.

## ÇıKıŞLAR

###  
**New-AzApplicationGatewayPathRuleConfig** , **Microsoft. Azure. Commands. Network. model. PSApplicationGatewayPathRule** nesnesinin yeni örneklerini oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[Yeni-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


