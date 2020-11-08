---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105664"
---
# Get-AzureApplicationGatewaySslCertificate

## SYNOPSIS
Uygulama ağ geçidi sertifikalarını alır.

## INDEKI

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureApplicationGatewaySslCertificate** cmdlet 'ı bir Azure Application Gateway Için güvenli yuva KATMANı (SSL) sertifikaları alır.

## ÖRNEKLERDEN

### Örnek 1: SSL sertifikası alın
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

Bu komut, ApplicationGateway08 adındaki uygulama ağ geçidinde SslCertificate13 adlı bir SSL sertifikası alır.

### Örnek 2: tüm SSL sertifikalarını edinin
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

Bu komut, ApplicationGateway08 adındaki uygulama ağ geçidinde tüm SSL sertifikalarını alır.

## PARAMETRELERINE

### -CertificateName
SSL sertifikasının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği sertifikayı alır.

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

### -Ad
Bu cmdlet 'in SSL sertifikası aldığı uygulama ağ geçidinin adını belirtir.

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
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, liste<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureApplicationGatewaySslCertificate](./Add-AzureApplicationGatewaySslCertificate.md)

[Remove-AzureApplicationGatewaySslCertificate](./Remove-AzureApplicationGatewaySslCertificate.md)
