---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: d9b1fd2f9161f9a717295d0995605eb6f75b8799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760864"
---
# Remove-AzEventGridTopic

## SYNOPSIS
Bir Azure olay Kılavuzu konusunu kaldırır.

## INDEKI

### TopicNameParameterSet (varsayılan)
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### TopicInputObjectParameterSet
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Bir Azure olay Kılavuzu konusunu kaldırır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunu kaldırır \` \` .

### Örnek 2
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunu kaldırır \` \` .

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
EventGrid konu RESOURCEID.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. EventGrid. modeller. PSTopic

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
