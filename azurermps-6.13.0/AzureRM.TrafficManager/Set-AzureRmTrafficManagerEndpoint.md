---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: a6a5b9ed5dbf1faa4a2be345039e53bb3daae291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587098"
---
# Set-AzureRmTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager uç noktasını güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzureRmTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'da uç noktayı güncelleştirir.
Bu cmdlet, yerel son nokta nesnesinden ayarları güncelleştirir.
*TrafficManagerEndpoint* parametresini kullanarak veya ardışık düzeni kullanarak uç nokta nesnesini belirtebilirsiniz.

Get-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktayı temsil eden yerel bir nesne edinebilirsiniz.
Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzureRmTrafficManagerEndpoint** kullanın.

## ÖRNEKLERDEN

### Örnek 1: uç noktayı güncelleştirme
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

İlk komut **Get-AzureRmTrafficManagerEndpoint** cmdlet 'ini kullanarak bir Azure Traffic Manager uç noktası alır.
Komut, uç noktayı $TrafficManagerEndpoint değişkeninde yerel olarak depolar.

İkinci komut, bu uç noktayı yerel olarak değiştirir.
Bu komut son nokta kalınlığını 20 olarak değiştirir.

Üçüncü komut, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.

## PARAMETRELERINE

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

### -TrafficManagerEndpoint
Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.
Bu cmdlet, Traffic Manager 'ı bu yerel nesneyle eşleşecek şekilde güncelleştirir.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Bu cmdlet bir **TrafficManagerEndpoint** nesnesini kabul eder.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Bu cmdlet bir **TrafficManagerEndpoint** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
