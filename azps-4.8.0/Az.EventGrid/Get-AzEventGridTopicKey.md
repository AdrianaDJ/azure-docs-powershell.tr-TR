---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109639"
---
# Get-AzEventGridTopicKey

## SYNOPSIS
Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.

## INDEKI

### TopicNameParameterSet (varsayılan)
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicInputObjectParameterSet
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Olay Kılavuzu konusunda etkinlikleri yayımlamak için kullanılan paylaşılan erişim tuşlarını alır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .

### Örnek 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun paylaşılan erişim anahtarlarını alır \` \` .

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

### -InputObject
EventGrid konu nesnesi.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. EventGrid. modeller. PSTopic

## ÇıKıŞLAR

### Microsoft. Azure. Management. EventGrid. modeller. TopicSharedAccessKeys

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
