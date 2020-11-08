---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276032"
---
# Get-AzPolicyMetadata

## SYNOPSIS
Ilke meta veri kaynaklarını alır

## INDEKI

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azilkedüzeltme** cmdlet 'i tüm ilke meta veri kaynaklarını veya belirli bir ilke meta veri kaynağını alır.

## ÖRNEKLERDEN

### Örnek 1: tüm ilke meta veri kaynaklarını alma
```powershell
PS C:\> Get-AzPolicyMetadata
```

Bu komut tüm ilke meta veri kaynaklarını alır

### Örnek 2:10 poliçe meta veri kaynağı topluluğunu alma
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

Bu komut 10 poliçe meta veri kaynağı koleksiyonunu alır

### Örnek 3: ' ACF1348 ' adlı tek bir ilke meta veri kaynağı alma
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

Bu komut, ' ACF1348 ' adlı tek bir ilke meta veri kaynağı alır

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

### -Ad
Kaynak adı.

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

### -Üst
Döndürülecek en fazla ilke meta veri kaynağı sayısı.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Policınsi. model. PSPolicyMetadata

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
