---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 03d85b0b31261330f6245e7439847df04d68d56b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591903"
---
# <span data-ttu-id="a23b2-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="a23b2-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="a23b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a23b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a23b2-103">Belirtilen konu için abonelik açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="a23b2-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a23b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a23b2-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a23b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a23b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a23b2-106">**Get-AzureRmServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu konusu için abonelik açıklaması döndürür.</span><span class="sxs-lookup"><span data-stu-id="a23b2-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="a23b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a23b2-107">EXAMPLES</span></span>

### <span data-ttu-id="a23b2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a23b2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="a23b2-109">Belirtilen hizmet veri yolu konusu için abonelik açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="a23b2-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="a23b2-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a23b2-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="a23b2-111">Belirtilen hizmet veri yolu konusu için Aboneliklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a23b2-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="a23b2-112">Varsayılan olarak, 100 abonelikleri geri döndürülecek; abonelik sayısı için lütfen-MaxCount parametresini kullanın</span><span class="sxs-lookup"><span data-stu-id="a23b2-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="a23b2-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a23b2-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="a23b2-114">Belirtilen hizmet veri yolu konusu için ilk 150 aboneliklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a23b2-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="a23b2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a23b2-115">PARAMETERS</span></span>

### <span data-ttu-id="a23b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23b2-116">-DefaultProfile</span></span>
<span data-ttu-id="a23b2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a23b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a23b2-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a23b2-118">-MaxCount</span></span>
<span data-ttu-id="a23b2-119">Döndürülecek maksimum abonelik sayısını saptayın.</span><span class="sxs-lookup"><span data-stu-id="a23b2-119">Determine the maximum number of Subscriptions to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23b2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a23b2-120">-Name</span></span>
<span data-ttu-id="a23b2-121">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="a23b2-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23b2-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a23b2-122">-Namespace</span></span>
<span data-ttu-id="a23b2-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="a23b2-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a23b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a23b2-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a23b2-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23b2-126">-Konu</span><span class="sxs-lookup"><span data-stu-id="a23b2-126">-Topic</span></span>
<span data-ttu-id="a23b2-127">Konu adı</span><span class="sxs-lookup"><span data-stu-id="a23b2-127">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23b2-128">CommonParameters</span></span>
<span data-ttu-id="a23b2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a23b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23b2-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a23b2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23b2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a23b2-131">INPUTS</span></span>

### <span data-ttu-id="a23b2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a23b2-132">System.String</span></span>

## <span data-ttu-id="a23b2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a23b2-133">OUTPUTS</span></span>

### <span data-ttu-id="a23b2-134">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="a23b2-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="a23b2-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a23b2-135">NOTES</span></span>

## <span data-ttu-id="a23b2-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a23b2-136">RELATED LINKS</span></span>
