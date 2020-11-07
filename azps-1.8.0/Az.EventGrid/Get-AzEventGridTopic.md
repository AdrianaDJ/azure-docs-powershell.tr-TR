---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760878"
---
# Get-AzEventGridTopic

## SYNOPSIS
Bir olay Kılavuzu konusunun ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.

## INDEKI

### ResourceGroupNameParameterSet (varsayılan)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzEventGridTopic cmdlet 'i, belirli bir olay Kılavuzu konusunun ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.
Konu adı sağlanmışsa, tek bir olay Kılavuzu konusunun ayrıntıları verilir.
Konu adı sağlanmadıysa, konu listesi döndürülür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .

### Örnek 2
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .

### Örnek 3
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Myresourcegroupname kaynak grubundaki tüm olay Kılavuzu konularını listeleyin \` \` .

### Örnek 4
```
PS C:\> Get-AzEventGridTopic
```

Abonelikteki tüm olay Kılavuzu konularını listeleyin.

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

### -Ad
EventGrid konu adı.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. EventGrid. modeller. PSTopic

### Microsoft. Azure. Commands. EventGrid. modeller. Pstopiclistınstance

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
