---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 67ce9249134365aa182024dff6e5913f68e11738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759135"
---
# <span data-ttu-id="c06c9-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c06c9-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="c06c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c06c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c06c9-103">Belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c06c9-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c06c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c06c9-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c06c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c06c9-105">DESCRIPTION</span></span>
<span data-ttu-id="c06c9-106">**Set-AzServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklama nesnesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c06c9-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c06c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c06c9-107">EXAMPLES</span></span>

### <span data-ttu-id="c06c9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c06c9-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="c06c9-109">Belirtilen konuyu belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c06c9-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="c06c9-110">Bu örnek, **Enableexpress** özelliğini **doğru** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c06c9-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="c06c9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c06c9-111">PARAMETERS</span></span>

### <span data-ttu-id="c06c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06c9-112">-DefaultProfile</span></span>
<span data-ttu-id="c06c9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c06c9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c06c9-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c06c9-114">-InputObject</span></span>
<span data-ttu-id="c06c9-115">ServiceBus konu tanımı.</span><span class="sxs-lookup"><span data-stu-id="c06c9-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c06c9-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c06c9-116">-Name</span></span>
<span data-ttu-id="c06c9-117">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="c06c9-117">Topic Name.</span></span>

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

### <span data-ttu-id="c06c9-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c06c9-118">-Namespace</span></span>
<span data-ttu-id="c06c9-119">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="c06c9-119">Namespace Name.</span></span>

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

### <span data-ttu-id="c06c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="c06c9-121">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="c06c9-121">The name of the resource group</span></span>

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

### <span data-ttu-id="c06c9-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="c06c9-122">-Confirm</span></span>
<span data-ttu-id="c06c9-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c06c9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06c9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06c9-124">-WhatIf</span></span>
<span data-ttu-id="c06c9-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c06c9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06c9-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c06c9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06c9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06c9-127">CommonParameters</span></span>
<span data-ttu-id="c06c9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c06c9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06c9-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c06c9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06c9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c06c9-130">INPUTS</span></span>

### <span data-ttu-id="c06c9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c06c9-131">System.String</span></span>

### <span data-ttu-id="c06c9-132">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="c06c9-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="c06c9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c06c9-133">OUTPUTS</span></span>

### <span data-ttu-id="c06c9-134">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="c06c9-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="c06c9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c06c9-135">NOTES</span></span>

## <span data-ttu-id="c06c9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c06c9-136">RELATED LINKS</span></span>
