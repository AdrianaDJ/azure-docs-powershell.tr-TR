---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3401010e1b65dbd0ad24f634c32b06449671419f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918375"
---
# New-AzApplicationGatewayConnectionDraining

## SYNOPSIS
Arka uç HTTP ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.

## INDEKI

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azapplicationgatewayconnectionboşaltma** cmdlet 'i arka uç http ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

Bu komut, Enabled değeri true olarak ayarlanmış yeni bir bağlantı boşaltma yapılandırması oluşturur ve DrainTimeoutInSec olarak 42 ayarlanır ve $connectionDraining içinde depolar.

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

### -DrainTimeoutInSec
Saniye bağlantısı boşaltma etkin.
Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.

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

### Özellikli
Bağlantı boşaltma 'nın etkin olup olmadığı.

```yaml
Type: System.Boolean
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

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azapplicationgatewayconnectionboşaltma](./Get-AzApplicationGatewayConnectionDraining.md)

[Remove-Azapplicationgatewayconnectionboşaltma](./Remove-AzApplicationGatewayConnectionDraining.md)

[Set-Azapplicationgatewayconnectionboşaltma](./Set-AzApplicationGatewayConnectionDraining.md)

