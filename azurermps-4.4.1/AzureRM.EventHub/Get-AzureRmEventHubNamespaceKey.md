---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594710"
---
# Get-AzureRmEventHubNamespaceKey

## SYNOPSIS
Belirtilen olay hub ad alanı yetkilendirme kuralındaki yetkilendirme kuralı için birincil, Ikincil ConnectionString ve Keys ayrıntılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## Tanım
Get-AzureRmEventHubNamespaceKey cmdlet 'i, verilen olay hub alanında belirtilen yetkilendirme kuralının birincil ve Ikincil ConnectionString ve anahtar ayrıntılarını döndürür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Birincil, Ikincil ConnectionString ve anahtarların, \` \` \` \` \` Myresourcegroupname kaynak grubunda yer alan Olay Hub 'ları ad alanı olan \` http

## PARAMETRELERINE

### -AuthorizationRuleName
Olay Hub 'Ları ad alanında yetkilendirme kuralının adı.

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

### Microsoft. Azure. Commands. EventHub. modeller. ListKeysAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

