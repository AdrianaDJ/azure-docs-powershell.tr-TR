---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 4daf2a86515522c3843d5d0225c133f0ff3686ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592596"
---
# Get-AzureRmOperationalInsightsSavedSearch

## SYNOPSIS
Belirtilen çalışma alanı için tüm kaydedilen aramaları döndürür.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermoperationalınsightssavedsearch** cmdlet 'i, kayıtlı BIR arama kimliği belirtmezseniz belirtilen kaynak grubundaki belirli bir çalışma alanı için kaydedilen aramaların tümünü döndürür.
Kayıtlı bir arama KIMLIĞI belirtirseniz, bu KIMLIĞE karşılık gelen kayıtlı arama döndürülür.

## ÖRNEKLERDEN

### Örnek 1: çalışma alanı için tüm kaydedilen aramaları alma
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

Bu komut, çalışma alanıyla ilişkilendirilmiş kaydedilmiş kaynakların tümünü alır.

### Örnek 2: KIMLIĞE göre kaydedilmiş belirli bir aramayı alma
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

Bu komut, belirli bir kaydedilmiş aramayı KIMLIĞIYLE alır.

## PARAMETRELERINE

### -ResourceGroupName
Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Savedsearchıd
Kayıtlı bir arama KIMLIĞI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Çalışmaalanıadı
Bir çalışma alanı adı belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Operationalınsights. model. Pssearchsearchlistlistresponse

### Microsoft. Azure. Commands. Operationalınsights. modeller

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure Operasyonel Öngörüler cmdlet 'Leri](./AzureRM.OperationalInsights.md)


