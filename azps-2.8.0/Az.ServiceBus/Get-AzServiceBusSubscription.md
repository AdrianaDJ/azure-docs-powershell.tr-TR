---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: bf6bd96314c8baf9e4d46b977b3f00457342db96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932474"
---
# <span data-ttu-id="286c3-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="286c3-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="286c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286c3-102">SYNOPSIS</span></span>
<span data-ttu-id="286c3-103">Belirtilen konu için abonelik açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="286c3-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="286c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="286c3-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="286c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="286c3-105">DESCRIPTION</span></span>
<span data-ttu-id="286c3-106">**Get-AzServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu konusu için abonelik açıklaması döndürür.</span><span class="sxs-lookup"><span data-stu-id="286c3-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="286c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="286c3-107">EXAMPLES</span></span>

### <span data-ttu-id="286c3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="286c3-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="286c3-109">Belirtilen hizmet veri yolu konusu için abonelik açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="286c3-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="286c3-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="286c3-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="286c3-111">Belirtilen hizmet veri yolu konusu için Aboneliklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="286c3-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="286c3-112">Varsayılan olarak, 100 abonelikleri geri döndürülecek; abonelik sayısı için lütfen-MaxCount parametresini kullanın</span><span class="sxs-lookup"><span data-stu-id="286c3-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="286c3-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="286c3-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="286c3-114">Belirtilen hizmet veri yolu konusu için ilk 150 aboneliklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="286c3-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="286c3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="286c3-115">PARAMETERS</span></span>

### <span data-ttu-id="286c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286c3-116">-DefaultProfile</span></span>
<span data-ttu-id="286c3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="286c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286c3-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="286c3-118">-MaxCount</span></span>
<span data-ttu-id="286c3-119">Döndürülecek maksimum abonelik sayısını saptayın.</span><span class="sxs-lookup"><span data-stu-id="286c3-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="286c3-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="286c3-120">-Name</span></span>
<span data-ttu-id="286c3-121">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="286c3-121">Subscription Name</span></span>

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

### <span data-ttu-id="286c3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="286c3-122">-Namespace</span></span>
<span data-ttu-id="286c3-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="286c3-123">Namespace Name</span></span>

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

### <span data-ttu-id="286c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="286c3-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="286c3-125">The name of the resource group</span></span>

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

### <span data-ttu-id="286c3-126">-Konu</span><span class="sxs-lookup"><span data-stu-id="286c3-126">-Topic</span></span>
<span data-ttu-id="286c3-127">Konu adı</span><span class="sxs-lookup"><span data-stu-id="286c3-127">Topic Name</span></span>

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

### <span data-ttu-id="286c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286c3-128">CommonParameters</span></span>
<span data-ttu-id="286c3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="286c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286c3-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286c3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286c3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="286c3-131">INPUTS</span></span>

### <span data-ttu-id="286c3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="286c3-132">System.String</span></span>

## <span data-ttu-id="286c3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="286c3-133">OUTPUTS</span></span>

### <span data-ttu-id="286c3-134">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="286c3-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="286c3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="286c3-135">NOTES</span></span>

## <span data-ttu-id="286c3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="286c3-136">RELATED LINKS</span></span>
