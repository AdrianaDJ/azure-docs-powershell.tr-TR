---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: d90d93548e46f3586319b0acf96319fe24e298af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594179"
---
# Get-AzureRmServiceBusQueue

## SYNOPSIS
Belirtilen hizmet veri yolu sırasının açıklamasını döndürür.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu sırasının açıklamasını döndürür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

Kuyruğun açıklamasını döndürür. 

## PARAMETRELERINE

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
Sıra adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
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

### -ResourceGroupName
Kaynak grubunun adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ServiceBus. model. QueueAttributes
LockDuration: AccessedAt: 1/1/0001 12:00:00 ısautodeleteononıdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:35 har DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false Enablebölümlendirme: true ısanonymouserişilebilirlik: yanlış MaxDeliveryCount: Maxsizeınmega: 16384 messagecount: CountDetails: Microsoft. Azure. Management. ServiceBus. modeller. messagecountdetails RequiresDuplicateDetection: false requires,/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/namespaces/SB-example1/Queues/S: false. SupportOrdering: B-Queue_example1 ad: SB-Queue_example1 tür: Microsoft. ServiceBus/Queues location: Batı ABD 1/20/2017 2:51:37

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

