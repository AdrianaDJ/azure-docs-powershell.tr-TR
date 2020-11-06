---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587781"
---
# New-AzureRmServiceBusQueueAuthorizationRule

## SYNOPSIS
Belirtilen hizmet veri yolu kuyruğu için yeni bir yetkilendirme kuralı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Yeni-Azurermservicebusqueuerule** cmdlet 'ı belirtilen hizmet veri yolu kuyruğu için yeni bir yetkilendirme kuralı oluşturur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

`SBAuthoRule1`Sıra Için **dinleme ve gönderme** haklarını içeren yetkilendirme kuralı oluşturur `SB-Queue_exampl1` .

## PARAMETRELERINE

### -ResourceGroup
Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hak
Hakları belirtir; Örneğin,  
@ ("Dinle", "Gönder", "Yönet")

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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
Default value: False
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
Default value: False
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

### -Ad
AuthorizationRule adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Ad alanı adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sıra
Sıra adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### -ResourceGroup
 System. String
 

### -NamespaceName
 System. String
 

### -SıraAdı
 System. String
 

### -AuthorizationRuleName
 System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes
ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizatı Irules/SBAuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 location: Batı US Etiketler: haklar: {Listen, gönder}

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

