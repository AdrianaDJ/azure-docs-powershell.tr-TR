---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 23392f77c9315cee2bf8b1b8369febbc2281c6ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937763"
---
# Get-AzEventGridTopicType

## SYNOPSIS
Azure olay Kılavuzu tarafından desteklenen konu türleriyle ilgili ayrıntıları alır.

## INDEKI

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Azure olay Kılavuzu tarafından desteklenen konu türlerinin ayrıntılarını alır.
Konu türü adı belirtilmişse, bu konu türüyle ilgili Ayrıntılar döndürülür.
Konu türü adı belirtilmezse, tüm konu türleriyle ilgili ayrıntılar verilir.
Includeeventtypes belirtildiğinde, her konu türü tarafından desteklenen olay türleriyle ilgili bilgiler yanıta dahildir.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

Konu türlerinin bir listesini alır.

### Örnek 2
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

StorageAccounts konu türü hakkında bilgi alır.

### Örnek 3
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Storageaccounts konu türüyle ilgili bilgileri, StorageAccounts tarafından desteklenen olay türleriyle birlikte alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Includeeventtypedata
Belirtilmişse, yanıt bir konu türü tarafından desteklenen olay türlerini içerecektir.

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

### -Ad
EventGrid konu türü adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypetypelistınstance

### Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypeınfo

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
