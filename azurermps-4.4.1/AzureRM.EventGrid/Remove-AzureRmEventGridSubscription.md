---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594724"
---
# Remove-AzureRmEventGridSubscription

## SYNOPSIS
Azure olay Kılavuzu olay aboneliğini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ResourceGroupNameParameterSet (varsayılan)
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Eventsubscriptionınputobjectset
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### TopicNameParameterSet
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
Azure olay Kılavuzu konusu, kaynak, Azure aboneliği veya kaynak grubu için bir Azure olay Kılavuzu olay aboneliğini kaldırır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Olay aboneliği EventSubscription1, \` \` \` \` myresourcegroupname kaynak grubundaki bir Azure olay kılavuzu konusuna konu1 \` \` .

### Örnek 2
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Olay aboneliği \` EventSubscription1 \` myresourcegroupname kaynak grubuna kaldırır \` \` .

### Örnek 3
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

Olay aboneliği EventSubscription1 ' \` nu \` varsayılan Azure aboneliği 'ne kaldırır.

### Örnek 4
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

Olay aboneliği \` EventSubscription1 \` bir olay hub ad alanına kaldırır.

### Örnek 5
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

Olay aboneliği \` EventSubscription1 \` bir olay kılavuzu konusuna kaldırır.

## PARAMETRELERINE

### -EventSubscriptionName
Kaldırılması gereken olay aboneliğinin adı.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
EventGrid Olayaboneliği nesnesi.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Geçiş
Kaldırma işleminin durumunu döndürür. Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Olay aboneliğinin kaldırılması gereken kaynağın tanıtıcısı.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
Olay Kılavuzu konu adı.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String
Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription

## ÇıKıŞLAR

### System. Object

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

