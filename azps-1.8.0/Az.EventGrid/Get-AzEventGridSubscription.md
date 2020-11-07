---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760880"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Bir olay aboneliğinin ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay aboneliklerinin listesini alır.

## INDEKI

### EventSubscriptionTopicNameParameterSet (varsayılan)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Get-AzEventGridSubscription cmdlet 'i, belirli bir olay Kılavuzu aboneliğinin ayrıntılarını veya geçerli Azure aboneliğindeki veya kaynak grubundaki tüm olay Kılavuzu aboneliklerinin listesini alır.
Olay aboneliği adı sağlanmışsa, tek bir olay Kılavuzu aboneliğinin ayrıntıları döndürülür.
Olay aboneliği adı sağlanmazsa, tüm olay abonelikleri listesi döndürülür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 EventSubscription1 için oluşturulan olay \` aboneliği ayrıntılarını alır \` .

### Örnek 2
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

\` \` \` \` \` \` Web kancası tabanlı bir olay aboneliği olan tam uç nokta URL 'si de dahil olmak üzere, myresourcegroupname kaynak grubundaki konu konu1 için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.

### Örnek 3
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

\` \` Myresourcegroupname kaynak grubunda konu konu1 için oluşturulan tüm olay aboneliklerinin bir listesini alın \` \` .

### Örnek 4
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

\` \` Myresourcegroupname kaynak grubu için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır \` \` .

### Örnek 5
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

\` \` Seçili Azure aboneliği için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.

### Örnek 6
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Myresourcegroupname kaynak grubu altında oluşturulan tüm genel olay aboneliklerinin listesini alır \` \` .

### Örnek 7
```
PS C:\> Get-AzEventGridSubscription
```

Seçili Azure aboneliği altında oluşturulan tüm genel olay aboneliklerinin listesini alır.

### Örnek 8
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

\` \` Belirtilen konum westus2 kaynak grubu altında oluşturulan tüm bölgesel olay aboneliklerinin listesini alır \` \` .

### Örnek 9
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Belirtilen EventHub ad alanı için oluşturulan tüm olay abonelikleri listesini alır.

### Örnek 10
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Belirtilen konu türü (EventHub ad alanları) için oluşturulan tüm olay aboneliklerinin listesini belirtilen konumda alır.

### Örnek 11
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Belirli bir kaynak grubu için oluşturulan tüm olay aboneliklerinin listesini alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -EventSubscriptionName
Olay aboneliğinin adı

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Olay aboneliği hedefinin tam uç nokta URL 'sini ekleyin.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid konu nesnesi.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Konum
Konumuyla

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Olay aboneliklerinin oluşturulduğu kaynağın tanıtıcısı.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
EventGrid konu adı.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType adı

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. EventGrid. modeller. PSTopic

## ÇıKıŞLAR

### Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
