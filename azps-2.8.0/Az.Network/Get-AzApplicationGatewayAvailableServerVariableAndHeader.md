---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8f0fc8caba03251ede507fc383ef99c10a06eeb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931815"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## SYNOPSIS
Desteklenen sunucu değişkenlerini ve kullanılabilir istek ve yanıt üst bilgilerini alın.

## INDEKI

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## Tanım
**Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet 'i, desteklenen sunucu değişkenlerini ve kullanılabilir istek ve yanıt üstbilgilerini alır. Parametreler, değişkenler veya üstbilgiler listelerini almak için kullanılabilir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

Bu komut, kullanılabilen tüm sunucu değişkenlerini döndürür.

### Örnek 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

Bu komut, kullanılabilen tüm istek üstbilgilerini döndürür.

### Örnek 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

Bu komut, kullanılabilir tüm yanıt üstbilgilerini döndürür.

### Örnek 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

Bu komut kullanılabilir tüm sunucu değişkenlerini, istek ve yanıt üstbilgilerini döndürür.

### Örnek 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

Bu komut kullanılabilir tüm sunucu değişkenlerini, istek ve yanıt üstbilgilerini döndürür.

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

### -RequestHeader
Uygulama ağ geçidi kullanılabilir istek üst bilgileri.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResponseHeader
Uygulama ağ geçidi kullanılabilir yanıt üst bilgileri.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerVariable
Uygulama ağ geçidi kullanılabilir sunucu değişkenleri.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## NOTLARıNDA
**List-AzApplicationGatewayAvailableServerVariableAndHeader** , **Get-azapplicationgatewayavailableservervariableveheader** cmdlet 'inin diğer adıdır.

## ILGILI BAĞLANTıLAR
