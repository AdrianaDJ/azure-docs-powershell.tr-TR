---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587669"
---
# Get-AzureRmBillingInvoice

## SYNOPSIS
Aboneliğin fatura faturalarını alma.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Liste (varsayılan)
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Sürümü
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Başına
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermbillingınvoice** cmdlet 'inin fatura faturalarını alır. 

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

Aboneliğin en son faturasını edinin.

### Örnek 2
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

Belirtilen ada sahip aboneliğin faturasını alın.

### Örnek 3
```
PS C:\> Get-AzureRmBillingInvoice
```

Aboneliğin tüm kullanılabilir faturalarını, indirme URL 'Si olmadan en son faturayla başlayan ters kronolojik sırada alın. 

### Örnek 4
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Aboneliğin en son 10 faturalarını alın ve indirme URL 'sini sonuç olarak ekleyin.

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

### -GenerateDownloadUrl
Faturaların indirme URL 'sini oluşturun.

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -En son
En son faturayı edinin.

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Döndürülecek en fazla kayıt sayısını belirler.

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
Bir veya en son belirtilmemişse, belirli bir faturanın adı.

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

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. faturalandırma. modeller. Invoice, Microsoft. Azure. Commands. Faturalandırma, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Management. faturalandırma. modeller. fatura

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

