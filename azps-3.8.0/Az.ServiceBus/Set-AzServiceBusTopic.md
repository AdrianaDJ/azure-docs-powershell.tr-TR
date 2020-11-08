---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104304"
---
# <span data-ttu-id="dcb38-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="dcb38-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="dcb38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcb38-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb38-103">Belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dcb38-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dcb38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcb38-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcb38-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcb38-105">DESCRIPTION</span></span>
<span data-ttu-id="dcb38-106">**Set-AzServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklama nesnesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dcb38-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dcb38-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcb38-107">EXAMPLES</span></span>

### <span data-ttu-id="dcb38-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcb38-108">Example 1</span></span>
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

<span data-ttu-id="dcb38-109">Belirtilen konuyu belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dcb38-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="dcb38-110">Bu örnek, **Enableexpress** özelliğini **doğru** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dcb38-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="dcb38-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcb38-111">PARAMETERS</span></span>

### <span data-ttu-id="dcb38-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb38-112">-DefaultProfile</span></span>
<span data-ttu-id="dcb38-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcb38-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcb38-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcb38-114">-InputObject</span></span>
<span data-ttu-id="dcb38-115">ServiceBus konu tanımı.</span><span class="sxs-lookup"><span data-stu-id="dcb38-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="dcb38-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcb38-116">-Name</span></span>
<span data-ttu-id="dcb38-117">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="dcb38-117">Topic Name.</span></span>

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

### <span data-ttu-id="dcb38-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dcb38-118">-Namespace</span></span>
<span data-ttu-id="dcb38-119">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="dcb38-119">Namespace Name.</span></span>

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

### <span data-ttu-id="dcb38-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcb38-120">-ResourceGroupName</span></span>
<span data-ttu-id="dcb38-121">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="dcb38-121">The name of the resource group</span></span>

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

### <span data-ttu-id="dcb38-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="dcb38-122">-Confirm</span></span>
<span data-ttu-id="dcb38-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dcb38-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcb38-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcb38-124">-WhatIf</span></span>
<span data-ttu-id="dcb38-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcb38-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcb38-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dcb38-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcb38-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb38-127">CommonParameters</span></span>
<span data-ttu-id="dcb38-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcb38-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb38-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb38-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb38-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcb38-130">INPUTS</span></span>

### <span data-ttu-id="dcb38-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dcb38-131">System.String</span></span>

### <span data-ttu-id="dcb38-132">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="dcb38-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="dcb38-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcb38-133">OUTPUTS</span></span>

### <span data-ttu-id="dcb38-134">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="dcb38-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="dcb38-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcb38-135">NOTES</span></span>

## <span data-ttu-id="dcb38-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcb38-136">RELATED LINKS</span></span>
