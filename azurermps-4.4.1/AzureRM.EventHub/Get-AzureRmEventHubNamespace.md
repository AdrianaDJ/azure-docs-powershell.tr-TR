---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593563"
---
# Get-AzureRmEventHubNamespace

## SYNOPSIS
Bir olay hub ad alanının ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## Tanım
Get-AzureRmEventHubNamespace cmdlet 'i, belirtilen bir olay hub ad alanının ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.
Ad alanı adı sağlanmışsa, tek bir olay hub ad alanının ayrıntıları verilir.
Ad alanı adı sağlanmazsa, ad alanları listesi döndürülür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

\` \` Myresourcegroupname kaynak grubundaki cynamespacadındaki Olay Hub ad alanının ayrıntılarını alır \` \` .

## PARAMETRELERINE

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
EventHub ad alanı adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. NamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

