---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105665"
---
# Get-AzureApplicationGatewayConfig

## SYNOPSIS
Uygulama ağ geçidi yapılandırma bağlamını alır.

## INDEKI

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureApplicationGatewayConfig** cmdlet 'ı bir Azure Application Gateway yapılandırma bağlamını alır.
Bağlam hem yapılandırma nesnesini hem de XML yapılandırmasını içerir.
XML yapılandırmasını dosyaya kaydedebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: uygulama ağ geçidi yapılandırmasını alma ve dosyaya kaydetme
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

Bu komut, ApplicationGateway06 adlı bir uygulama ağ geçidinin yapılandırmasını alır.
Komut dosyayı belirtilen yolda kaydeder.

## PARAMETRELERINE

### -ExportToFile
Bu cmdlet 'in yapılandırmayı XML biçiminde kaydettiği bir dosya yolu belirtir.

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
Bu cmdlet 'in yapılandırma bilgilerini aldığı uygulama ağ geçidinin adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureApplicationGatewayConfig](./Set-AzureApplicationGatewayConfig.md)


