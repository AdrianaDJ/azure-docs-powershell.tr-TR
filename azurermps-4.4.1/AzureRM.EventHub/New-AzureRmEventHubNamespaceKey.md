---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594704"
---
# New-AzureRmEventHubNamespaceKey

## SYNOPSIS
Belirtilen olay hub ad boşluğunda yetkilendirme kuralı için yeni bir birincil veya ikincil anahtar oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## Tanım
New-AzureRmEventHubNamespaceKey cmdlet, belirtilen etkinlik hub ad boşluğunda verilen yetkilendirme kuralı için birincil veya ikincil anahtarı oluşturur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

\` \` \` \` Myresourcegroupname kaynak grubuyla, Cynamespacadındaki Olay Hub 'ları ad alanında myauthrulename birincil anahtarını yeniden oluşturur \` \` .

## PARAMETRELERINE

### -AuthorizationRuleName
Yetkilendirme kuralı adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -RegenerateKeys
Yeniden oluşturmak için anahtar: \` PrimaryKey \` veya \` secondarykey \` .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Kaynak grubunun adı.

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

### Microsoft. Azure. Commands. EventHub. modeller. ListKeysAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

