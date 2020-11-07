---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 217b9f8775f38635cf2285215a0be10a92b832c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753945"
---
# Get-AzStreamAnalyticsDefaultFunctionDefinition

## SYNOPSIS
Stream Analytics 'te bir işlevin varsayılan tanımını alır.

## INDEKI

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet 'ı, Azure Stream Analytics 'te bir işlevin varsayılan tanımını alır.
İşlev oluşturmak için varsayılan tanımı ve New-AzStreamAnalyticsFunction cmdlet 'ini kullanabilirsiniz.
Bir işlev oluşturmadan önce varsayılan tanımı değiştirebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: Stream Analytics işlevinin varsayılan tanımını alma
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

Bu komut, RetrieveDefaultDefinitionRequest.jsdosyasındaki ScoreTweet adlı işlevin varsayılan tanımını alır.

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

### -Dosya
Varsayılan işlev tanımı alma isteğine ait istek gövdesinin JavaScript nesne Gösterim (JSON) gösterimini içeren bir. json dosyasının yolunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
İşlevlerin ait olduğu Stream Analytics işinin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği iş için varsayılan tanımı alır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in varsayılan tanımı aldığı Stream Analytics işlevinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Stream Analytics işlevlerinin ait olduğu kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği grup için bir işlev tanımı alır.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzStreamAnalyticsFunction](./New-AzStreamAnalyticsFunction.md)


