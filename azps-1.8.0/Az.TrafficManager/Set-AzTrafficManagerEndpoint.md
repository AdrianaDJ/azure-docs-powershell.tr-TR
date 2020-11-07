---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 31201d607d1b9f0825236fe162bf86028b148193
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753861"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager uç noktasını güncelleştirir.

## INDEKI

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzTrafficManagerEndpoint** cmdlet 'ı Azure Traffic Manager 'da uç noktayı güncelleştirir.
Bu cmdlet, yerel son nokta nesnesinden ayarları güncelleştirir.
*TrafficManagerEndpoint* parametresini kullanarak veya ardışık düzeni kullanarak uç nokta nesnesini belirtebilirsiniz.

Get-AzTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktayı temsil eden yerel bir nesne edinebilirsiniz.
Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzTrafficManagerEndpoint** kullanın.

## ÖRNEKLERDEN

### Örnek 1: uç noktayı güncelleştirme
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

İlk komut **Get-AzTrafficManagerEndpoint** cmdlet 'ini kullanarak bir Azure Traffic Manager uç noktası alır.
Komut, uç noktayı $TrafficManagerEndpoint değişkeninde yerel olarak depolar.

İkinci komut, bu uç noktayı yerel olarak değiştirir.
Bu komut son nokta kalınlığını 20 olarak değiştirir.

Üçüncü komut, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.

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

### Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint

## ÇıKıŞLAR

### Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
