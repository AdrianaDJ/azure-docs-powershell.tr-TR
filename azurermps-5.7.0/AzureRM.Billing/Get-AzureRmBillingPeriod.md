---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594139"
---
# Get-AzureRmBillingPeriod

## SYNOPSIS
Aboneliğin fatura dönemlerini alın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Liste (varsayılan)
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Başına
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermbillingdönem** cmdlet 'i aboneliğin fatura dönemlerini alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmBillingPeriod
```

Aboneliğin tüm kullanılabilir fatura dönemlerini edinin.

### Örnek 2
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

Belirtilen ada sahip aboneliğin fatura dönemini alın.

### Örnek 3
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

Aboneliğin en fazla 2 fatura dönemini alın.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -MaxCount
Döndürülecek en fazla kayıt sayısını belirleme.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak belirli bir fatura döneminin adı.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem, Microsoft. Azure. Commands. Faturalandırma, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. faturalandırma. modeller. Psbillingdönem

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

