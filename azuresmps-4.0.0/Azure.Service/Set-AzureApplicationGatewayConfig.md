---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106429"
---
# Set-AzureApplicationGatewayConfig

## SYNOPSIS
Uygulama ağ geçidi yapılandırır.

## INDEKI

### configFile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureApplicationGatewayConfig** cmdlet 'i bir uygulama ağ geçidi yapılandırır.

## ÖRNEKLERDEN

### Örnek 1: yapılandırma nesnesi kullanarak uygulama ağ geçidi yapılandırma
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

İlk komut **Get-AzureApplicationGatewayConfig** cmdlet 'Ini kullanarak ApplicationGateway02 adındaki uygulama ağ geçidi için yapılandırma nesnesini alır.
Komut, $ConfigReturnObject değişkeninde depolar.

İkinci komut, $ConfigReturnObject değişkeninde depolanan bir uygulama ağ geçidi yapılandırma nesnesini kullanarak, ApplicationGateway06 adındaki uygulamanın yapılandırmasını ayarlar.

### Örnek 2: yapılandırma dosyası kullanarak uygulama ağ geçidi yapılandırma
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

Bu komut, ApplicationGateway06 adındaki uygulamanın yapılandırmasını belirtilen konumda bir uygulama ağ geçidi yapılandırma dosyasını kullanarak ayarlar.

### Örnek 3: yapılandırma nesnesi kullanarak yapılandırmayı değiştirme
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

İlk komut **Get-AzureApplicationGatewayConfig** cmdlet 'Ini kullanarak ApplicationGateway06 adındaki uygulama ağ geçidi için yapılandırma nesnesini alır.
Komut, $ConfigReturnObject değişkeninde depolar.

İkinci komut, $ConfigReturnObject depolanan nesnedeki bir **bağlantı noktası** özelliğine bir bağlantı noktası değeri atar.

Son komutu, güncelleştirilmiş $ConfigReturnObject geçerli cmdlet 'e geçirir.

## PARAMETRELERINE

### -Config
Uygulama ağ geçidi yapılandırma nesnesini belirtir.
Bu cmdlet, bu parametrenin bir uygulama ağ geçidine belirttiği yapılandırmayı atar.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Configfıle
Uygulama ağ geçidi için yapılandırma dosyasının yolunu XML biçiminde belirtir.
Bu cmdlet, bu parametrenin bir uygulama ağ geçidine belirttiği yapılandırmayı atar.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in yapılandırdığı uygulama ağ geçidinin adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## ÇıKıŞLAR

### Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


