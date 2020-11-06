---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ca03b95748203546fb8d9235cb7822a4dde359a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594230"
---
# New-AzureRmApplicationGatewayConnectionDraining

## SYNOPSIS
Arka uç HTTP ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzureRmApplicationGatewayConnectionDraining** cmdlet 'i arka uç http ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

Bu komut, Enabled değeri true olarak ayarlanmış yeni bir bağlantı boşaltma yapılandırması oluşturur ve DrainTimeoutInSec olarak 42 ayarlanır ve $connectionDraining içinde depolar.

## PARAMETRELERINE

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmApplicationGatewayConnectionDraining](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[Remove-AzureRmApplicationGatewayConnectionDraining](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[Set-AzureRmApplicationGatewayConnectionDraining](./Set-AzureRmApplicationGatewayConnectionDraining.md)

