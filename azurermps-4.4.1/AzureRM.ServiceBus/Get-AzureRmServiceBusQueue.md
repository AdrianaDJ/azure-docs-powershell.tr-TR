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
# <span data-ttu-id="f32e3-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f32e3-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="f32e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f32e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f32e3-103">Belirtilen hizmet veri yolu sırasının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f32e3-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f32e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f32e3-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f32e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f32e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f32e3-106">**Get-AzureRmServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu sırasının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f32e3-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="f32e3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f32e3-107">EXAMPLES</span></span>

### <span data-ttu-id="f32e3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f32e3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

<span data-ttu-id="f32e3-109">Kuyruğun açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f32e3-109">Returns the description of the queue.</span></span> 

## <span data-ttu-id="f32e3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f32e3-110">PARAMETERS</span></span>

### <span data-ttu-id="f32e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32e3-111">-DefaultProfile</span></span>
<span data-ttu-id="f32e3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f32e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f32e3-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f32e3-113">-Name</span></span>
<span data-ttu-id="f32e3-114">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="f32e3-114">Queue Name.</span></span>

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

### <span data-ttu-id="f32e3-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f32e3-115">-Namespace</span></span>
<span data-ttu-id="f32e3-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="f32e3-116">Namespace Name.</span></span>

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

### <span data-ttu-id="f32e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="f32e3-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="f32e3-118">The name of the resource group</span></span>

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

### <span data-ttu-id="f32e3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32e3-119">CommonParameters</span></span>
<span data-ttu-id="f32e3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f32e3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32e3-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f32e3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32e3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f32e3-122">INPUTS</span></span>

### <span data-ttu-id="f32e3-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f32e3-123">-ResourceGroup</span></span>
 <span data-ttu-id="f32e3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f32e3-124">System.String</span></span>
 

### <span data-ttu-id="f32e3-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f32e3-125">-NamespaceName</span></span>
 <span data-ttu-id="f32e3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f32e3-126">System.String</span></span>
 

### <span data-ttu-id="f32e3-127">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="f32e3-127">-QueueName</span></span>
 <span data-ttu-id="f32e3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f32e3-128">System.String</span></span> 

## <span data-ttu-id="f32e3-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f32e3-129">OUTPUTS</span></span>

### <span data-ttu-id="f32e3-130">Microsoft. Azure. Commands. ServiceBus. model. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="f32e3-130">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="f32e3-131">LockDuration: AccessedAt: 1/1/0001 12:00:00 ısautodeleteononıdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:35 har DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false Enablebölümlendirme: true ısanonymouserişilebilirlik: yanlış MaxDeliveryCount: Maxsizeınmega: 16384 messagecount: CountDetails: Microsoft. Azure. Management. ServiceBus. modeller. messagecountdetails RequiresDuplicateDetection: false requires,/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/namespaces/SB-example1/Queues/S: false. SupportOrdering: B-Queue_example1 ad: SB-Queue_example1 tür: Microsoft. ServiceBus/Queues location: Batı ABD 1/20/2017 2:51:37</span><span class="sxs-lookup"><span data-stu-id="f32e3-131">LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:35 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 Name                                : SB-Queue_example1 Type                                : Microsoft.ServiceBus/Queues Location                            : West US</span></span>

## <span data-ttu-id="f32e3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f32e3-132">NOTES</span></span>

## <span data-ttu-id="f32e3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f32e3-133">RELATED LINKS</span></span>

