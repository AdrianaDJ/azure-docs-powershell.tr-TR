---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592524"
---
# New-AzureRmAnalysisServicesFirewallRule

## SYNOPSIS
Yeni bir Analysis Services güvenlik duvarı kuralı oluşturur

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## Tanım
New-AzureRmAnalysisServicesFirewallRule yeni bir güvenlik duvarı kuralı nesnesi oluşturur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

Başlangıç aralığı 0.0.0.0 ve bitiş aralığı 255.255.255.255 olan rule1 adlı bir güvenlik duvarı kuralı oluşturur

## PARAMETRELERINE

### -FirewallRuleName
Güvenlik duvarı kuralının adı

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RangeStart
Güvenlik duvarının başlangıç aralığı

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RangeEnd
Güvenlik duvarı kuralının Aralık sonu

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesFirewallRule

## ILGILI BAĞLANTıLAR

[New-AzureRmAnalysisServicesFirewallConfig](./New-AzureRmAnalysisServicesFirewallConfig.md)
