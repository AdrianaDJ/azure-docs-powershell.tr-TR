---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760408"
---
# New-AzApplicationGatewayFrontendPort

## SYNOPSIS
Uygulama ağ geçidi için ön uç bağlantı noktası oluşturur.

## INDEKI

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Yeni-Azapplicationgatewayfrontenvseçport** cmdlet 'ı bir Azure uygulama ağ geçidi için ön uç bağlantı noktası oluşturur.

## ÖRNEKLERDEN

### Example1: ön uç bağlantı noktası oluşturma
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

Bu komut FrontEndPort01 adlı bir ön uç bağlantı noktası 80 bağlantı noktası oluşturur ve sonucu $FrontEndPort adlı değişkende depolar.

## PARAMETRELERINE

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

### -Ad
Bu cmdlet 'in oluşturduğu ön uç bağlantı noktasının adını belirtir.

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

### -Bağlantı noktası
Ön uç bağlantı noktasının bağlantı noktası numarasını belirtir.

```yaml
Type: System.Int32
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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azapplicationgatewayfrontenvseçport](./Add-AzApplicationGatewayFrontendPort.md)

[Get-Azapplicationgatewayfrontenvseçport](./Get-AzApplicationGatewayFrontendPort.md)

[Remove-Azapplicationgatewayfrontenvseçport](./Remove-AzApplicationGatewayFrontendPort.md)

[Set-Azapplicationgatewayfrontenvseçport](./Set-AzApplicationGatewayFrontendPort.md)


