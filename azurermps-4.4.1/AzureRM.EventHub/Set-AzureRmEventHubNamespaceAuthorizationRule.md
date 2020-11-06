---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595174"
---
# Set-AzureRmEventHubNamespaceAuthorizationRule

## SYNOPSIS
Belirtilen olay hub isim uzayındaki yetkilendirme kuralını güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## Tanım
Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet 'i belirtilen etkinlik hub isim uzayındaki yetkilendirme kuralını güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

\`Yönetim haklarını sağlamak için myauthrulename yetkilendirme kuralını güncelleştirir \` .

## PARAMETRELERINE

### -AuthorizationRuleName
Yetkilendirme kuralı adı.
Gerekli Eğer-AuthruleObj belirtilmemişse.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuthRuleObj
Olay Hub 'Ları ad alanı yetkilendirme kuralı nesnesi.

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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

### -Hak
Gerekli Eğer-AuthruleObj belirtilmemişse.
Larım Örneğin, @ ("Dinle", "Gönder", "Yönet")

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. EventHub. model. SharedAccessAuthorizationRuleAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

