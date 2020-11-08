---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107605"
---
# <span data-ttu-id="2e87f-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="2e87f-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="2e87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e87f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e87f-103">Belirtilen hizmet veri yolu ad alanındaki hizmet veri yolu sırasının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e87f-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2e87f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e87f-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e87f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e87f-105">DESCRIPTION</span></span>
<span data-ttu-id="2e87f-106">**Set-AzServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki hizmet veri yolu sırasının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e87f-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2e87f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e87f-107">EXAMPLES</span></span>

### <span data-ttu-id="2e87f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2e87f-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
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
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="2e87f-109">Belirtilen sırayı belirtilen ad alanında yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e87f-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="2e87f-110">Bu örnek **DeadLetteringOnMessageExpiration** özelliğini **true** ve **SupportOrdering** 'i **true** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e87f-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="2e87f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e87f-111">PARAMETERS</span></span>

### <span data-ttu-id="2e87f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e87f-112">-DefaultProfile</span></span>
<span data-ttu-id="2e87f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e87f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e87f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e87f-114">-InputObject</span></span>
<span data-ttu-id="2e87f-115">ServiceBus tanımı.</span><span class="sxs-lookup"><span data-stu-id="2e87f-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e87f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e87f-116">-Name</span></span>
<span data-ttu-id="2e87f-117">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="2e87f-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e87f-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e87f-118">-Namespace</span></span>
<span data-ttu-id="2e87f-119">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2e87f-119">Namespace Name.</span></span>

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

### <span data-ttu-id="2e87f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e87f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e87f-121">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2e87f-121">The name of the resource group</span></span>

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

### <span data-ttu-id="2e87f-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e87f-122">-Confirm</span></span>
<span data-ttu-id="2e87f-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e87f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e87f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e87f-124">-WhatIf</span></span>
<span data-ttu-id="2e87f-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e87f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e87f-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e87f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e87f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e87f-127">CommonParameters</span></span>
<span data-ttu-id="2e87f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e87f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e87f-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e87f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e87f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e87f-130">INPUTS</span></span>

### <span data-ttu-id="2e87f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2e87f-131">System.String</span></span>

### <span data-ttu-id="2e87f-132">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="2e87f-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="2e87f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e87f-133">OUTPUTS</span></span>

### <span data-ttu-id="2e87f-134">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="2e87f-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="2e87f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e87f-135">NOTES</span></span>

## <span data-ttu-id="2e87f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e87f-136">RELATED LINKS</span></span>
