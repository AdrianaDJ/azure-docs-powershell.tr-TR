---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931758"
---
# Get-AzExpressRoutePortsLocation

## SYNOPSIS
ExpressRoutePort kaynaklarının kullanılabileceği konumları alır.

## INDEKI

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
ExpressRoutePort kaynaklarının kullanılabileceği konumları almak için **Get-AzExpressRoutePortsLocation** cmdlet 'i kullanılır. Giriş olarak belirli bir konum verildiğinde cmdlet bu konumun (yani, bu konumda kullanılabilir bant genişlikleri listesi) ayrıntılarını görüntüler.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

ExpressRoutePort kaynaklarının kullanılabileceği konumları listeler.

### Örnek 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

$Loc konumunda bulunan ExpressRoutePort bant genişliklerini listeler.

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

### -LocationName
Konumun adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSExpressRoutePortsLocation

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
