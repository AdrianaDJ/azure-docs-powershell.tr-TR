---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594714"
---
# Get-AzureRmEventHubConsumerGroup

## SYNOPSIS
Belirli bir olay hub tüketici grubunun ayrıntılarını alır veya bir olay hub 'ındaki tüketici gruplarının listesini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## Tanım
Get-AzureRmEventHubConsumerGroup cmdlet 'i, belirtilen bir olay hub tüketici grubunun ayrıntılarını veya belirli bir olay hub 'ındaki tüketici gruplarının listesini alır.
Tüketici grubunun adı sağlanmışsa, tek bir tüketici grubu ayrıntılarının ayrıntıları verilir.
Tüketici grubunun adı sağlanmadıysa, belirtilen olay hub 'ındaki tüketici gruplarının listesi döndürülür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla Adynamespacename ad alanında bulunan Olay Hub myeventhubname myconsumergroupname adlı \` Tüketici grubunu alır \` .

### Örnek 2
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

\` \` \` \` Myresourcegroupname kaynak grubuyla Mynamespacename ad alanında bulunan Olay Hub myeventhubname içindeki tüketici \` gruplarının bir listesini alır \` .

## PARAMETRELERINE

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

### -EventHub
EventHub adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
ConsumerGroup adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Ad alanı adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub., Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

