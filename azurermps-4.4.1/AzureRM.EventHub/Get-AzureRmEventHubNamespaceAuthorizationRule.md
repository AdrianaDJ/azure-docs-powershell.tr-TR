---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764856"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## SYNOPSIS
Bir Eventubs ad alanı yetkilendirme kuralının ayrıntılarını alır veya yetkilendirme kuralları listesini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## Tanım
Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet 'i, belirtilen bir olay hub ad alanı yetkilendirme kuralının ayrıntılarını veya ad alanı yetkilendirme kuralları listesini alır.
Yetkilendirme kuralı adı sağlanmışsa, tek bir yetkilendirme kuralının ayrıntıları verilir.
Yetkilendirme kuralı adı sağlanmazsa, ad alanındaki tüm yetkilendirme kurallarının bir listesi döndürülür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

\` \` \` \` Myresourcegroupname kaynak grubuyla birlikte, Cynamespacadındaki Olay Hub 'ları \` ad \`

### Örnek 2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

\` \` Olay Hub RootManageSharedAccessKey ad alanında \` \` , \` myresourcegroupname kaynak grubuyla, \` varsayılan yetkilendirme kuralı.

### Örnek 3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Olay Hub 'Ları ad alanı olan tüm yetkilendirme kurallarını \` \` myresourcegroupname kaynak grubuyla birlikte döndürür \` \` .

## PARAMETRELERINE

### -AuthorizationRuleName
Olay Hub 'Ları ad alanı yetkilendirme kuralı adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
Olay Hub 'Ları ad alanı adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

