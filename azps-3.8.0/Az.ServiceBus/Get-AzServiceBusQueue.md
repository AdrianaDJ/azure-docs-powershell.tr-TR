---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103739"
---
# <span data-ttu-id="8ea99-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="8ea99-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="8ea99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea99-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea99-103">Belirtilen hizmet veri yolu sırasının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ea99-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="8ea99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ea99-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ea99-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ea99-105">DESCRIPTION</span></span>
<span data-ttu-id="8ea99-106">Belirtilen hizmet veri yolu sırasının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ea99-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="8ea99-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ea99-107">EXAMPLES</span></span>

### <span data-ttu-id="8ea99-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8ea99-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="8ea99-109">Kuyruğun açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ea99-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="8ea99-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8ea99-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="8ea99-111">Verilen ad alanı için sıraların listesini döndürür; varsayılan olarak, 100 kuyrukları geri döndürülecek, en az 100 kuyruktan fazlası döndürülürse, lütfen-MaxCount parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8ea99-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="8ea99-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8ea99-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="8ea99-113">Verilen ad alanı için ilk 150 sıralarının listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="8ea99-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="8ea99-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ea99-114">PARAMETERS</span></span>

### <span data-ttu-id="8ea99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea99-115">-DefaultProfile</span></span>
<span data-ttu-id="8ea99-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ea99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ea99-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8ea99-117">-MaxCount</span></span>
<span data-ttu-id="8ea99-118">Döndürülecek en fazla sıra sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="8ea99-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="8ea99-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ea99-119">-Name</span></span>
<span data-ttu-id="8ea99-120">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="8ea99-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea99-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ea99-121">-Namespace</span></span>
<span data-ttu-id="8ea99-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="8ea99-122">Namespace Name</span></span>

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

### <span data-ttu-id="8ea99-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea99-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ea99-124">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="8ea99-124">The name of the resource group</span></span>

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

### <span data-ttu-id="8ea99-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea99-125">CommonParameters</span></span>
<span data-ttu-id="8ea99-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ea99-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea99-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea99-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea99-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ea99-128">INPUTS</span></span>

### <span data-ttu-id="8ea99-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8ea99-129">System.String</span></span>

## <span data-ttu-id="8ea99-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ea99-130">OUTPUTS</span></span>

### <span data-ttu-id="8ea99-131">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="8ea99-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="8ea99-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ea99-132">NOTES</span></span>

## <span data-ttu-id="8ea99-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ea99-133">RELATED LINKS</span></span>
