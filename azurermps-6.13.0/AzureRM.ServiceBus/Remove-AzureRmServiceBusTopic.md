---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587158"
---
# Remove-AzureRmServiceBusTopic

## SYNOPSIS
Belirtilen hizmet veri yolu ad boşluğundan konuyu kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Topıcpropertiesset (varsayılan)
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### TopicInputObjectSet
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Topicresourceıdset
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmServiceBusTopic** cmdlet 'i, konuyu belirtilen hizmet veri yolu ad boşluğundan kaldırır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

Başlığı `SB-Topic_exampl1` ad alanından kaldırır `SB-Example1` .

### Örnek 2,1-InputObject-değişken kullanan:
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### Örnek 2,2-InputObject-boru kullanarak:
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### Örnek 3,1-değişken kullanan RESOURCEID:
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### Örnek 3,2-dize değeri kullanma
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

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

### -InputObject
Hizmet veri yolu konu nesnesi

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Konu adı

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Ad alanı adı

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.

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
Kaynak grubunun adı

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Hizmet veri yolu başlığı kaynak kimliği

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
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

### Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri
Parametreler: InputObject (ByValue)

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
