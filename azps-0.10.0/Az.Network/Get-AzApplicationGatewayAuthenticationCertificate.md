---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935604"
---
# Get-AzApplicationGatewayAuthenticationCertificate

## SYNOPSIS
Uygulama ağ geçidi için kimlik doğrulama sertifikası alır.

## INDEKI

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzApplicationGatewayAuthenticationCertificate** cmdlet 'ı bir Azure uygulama ağ geçidi için kimlik doğrulama sertifikası alır.

## ÖRNEKLERDEN

### 2
```

```

## PARAMETRELERINE

### -ApplicationGateway
Bu cmdlet 'in kimlik doğrulama sertifikası aldığı uygulama ağ geçidi adını belirtir.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Bu cmdlet 'in aldığı kimlik doğrulama sertifikasının adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ

## ILGILI BAĞLANTıLAR

[Add-AzApplicationGatewayAuthenticationCertificate](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[Yeni-AzApplicationGatewayAuthenticationCertificate](./New-AzApplicationGatewayAuthenticationCertificate.md)

[Remove-AzApplicationGatewayAuthenticationCertificate](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[Set-AzApplicationGatewayAuthenticationCertificate](./Set-AzApplicationGatewayAuthenticationCertificate.md)


