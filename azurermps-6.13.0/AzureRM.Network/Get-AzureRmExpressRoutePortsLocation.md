---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764622"
---
# Get-AzureRmExpressRoutePortsLocation

## SYNOPSIS
ExpressRoutePort kaynaklarının kullanılabileceği konumları alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmExpressRoutePortsLocation** cmdlet 'ı ExpressRoutePort kaynaklarının kullanılabileceği konumları almak için kullanılır. Giriş olarak belirli bir konum verildiğinde cmdlet bu konumun (yani, bu konumda kullanılabilir bant genişlikleri listesi) ayrıntılarını görüntüler.


## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

ExpressRoutePort kaynaklarının kullanılabileceği konumları listeler.

### Örnek 2
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

$Loc konumunda bulunan ExpressRoutePort bant genişliklerini listeler.

## PARAMETRELERINE

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

### -LocationName
Konumun adı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSExpressRoutePortsLocation

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
