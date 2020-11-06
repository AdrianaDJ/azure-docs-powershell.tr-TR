---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587787"
---
# Get-AzureRmServiceBusTopic

## SYNOPSIS
Belirtilen hizmet veri yolu konusu için bir açıklama döndürür.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanı için bir konu açıklaması döndürür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

Verilen hizmet veri yolu ad alanı için belirtilen konunun açıklamasını döndürür.

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
Konu adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

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
 

### -TopicName
 System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ServiceBus. model. TopicAttributes
Ad: SB-Topic_exampl1 konum: Batı ABD kimliği:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 tür: Microsoft. ServiceBus/topic AccessedAt: 1/20/2017 3:18:54 ÖKÜONONONıDLE: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41:10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false enablebölümlendirme: true Enablesubscriptionbölümlendirme: false Filteringiletiedanör: false ısanonymouseriþin: false IsExpress: false Maxsizeınmega: 16384 requiresduplicatedetection: false sizeInBytes: 0 1/20/2017 3:16:43

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

