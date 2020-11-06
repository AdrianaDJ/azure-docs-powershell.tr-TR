---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 4b346d1ef4757d74ac9c663f5c72a134d5c48153
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590624"
---
# <span data-ttu-id="07047-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="07047-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="07047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07047-102">SYNOPSIS</span></span>
<span data-ttu-id="07047-103">Belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07047-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07047-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07047-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07047-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07047-105">DESCRIPTION</span></span>
<span data-ttu-id="07047-106">**Set-AzureRmServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklama nesnesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07047-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="07047-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07047-107">EXAMPLES</span></span>

### <span data-ttu-id="07047-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07047-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj
```

<span data-ttu-id="07047-109">Belirtilen konuyu belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07047-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="07047-110">Bu örnek, **Enableexpress** özelliğini **doğru** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07047-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="07047-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07047-111">PARAMETERS</span></span>

### <span data-ttu-id="07047-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="07047-112">-Confirm</span></span>
<span data-ttu-id="07047-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07047-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07047-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07047-114">-WhatIf</span></span>
<span data-ttu-id="07047-115">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07047-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07047-116">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07047-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07047-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07047-117">-DefaultProfile</span></span>
<span data-ttu-id="07047-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07047-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07047-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07047-119">-InputObject</span></span>
<span data-ttu-id="07047-120">ServiceBus konu tanımı.</span><span class="sxs-lookup"><span data-stu-id="07047-120">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07047-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="07047-121">-Name</span></span>
<span data-ttu-id="07047-122">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="07047-122">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07047-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07047-123">-Namespace</span></span>
<span data-ttu-id="07047-124">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="07047-124">Namespace Name.</span></span>

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

### <span data-ttu-id="07047-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07047-125">-ResourceGroupName</span></span>
<span data-ttu-id="07047-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="07047-126">The name of the resource group</span></span>

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

### <span data-ttu-id="07047-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07047-127">CommonParameters</span></span>
<span data-ttu-id="07047-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07047-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07047-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07047-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07047-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07047-130">INPUTS</span></span>

### <span data-ttu-id="07047-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="07047-131">-ResourceGroup</span></span>
 <span data-ttu-id="07047-132">System. String</span><span class="sxs-lookup"><span data-stu-id="07047-132">System.String</span></span>

### <span data-ttu-id="07047-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="07047-133">-NamespaceName</span></span>
 <span data-ttu-id="07047-134">System. String</span><span class="sxs-lookup"><span data-stu-id="07047-134">System.String</span></span>

### <span data-ttu-id="07047-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="07047-135">-TopicName</span></span>
 <span data-ttu-id="07047-136">System. String</span><span class="sxs-lookup"><span data-stu-id="07047-136">System.String</span></span>

### <span data-ttu-id="07047-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="07047-137">-TopicObj</span></span>
 <span data-ttu-id="07047-138">Microsoft. Azure. Commands. ServiceBus. model. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="07047-138">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>

## <span data-ttu-id="07047-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07047-139">OUTPUTS</span></span>

### <span data-ttu-id="07047-140">Microsoft. Azure. Commands. ServiceBus. model. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="07047-140">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="07047-141">Ad: SB-Topic_exampl1 konum: Batı ABD kimliği:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1 tür: Microsoft. ServiceBus/topic AccessedAt: 1/20/2017 3:18:54 har Autodeleteonıdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 har Sayaçdetails: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: doğru Enablehızlı: doğru Enablebölümlendirme: true Enablesubscriptionbölümlendirme: false Filteringiletiedanör: false ısanonymouseriþin: false IsExpress: false Maxsizeınmega: 16384 RequiresDuplicateDetection: false sizeInBytes: 0 durum: Active SubscriptionCount: 1 SupportOrdering: false UpdatedAt: 1/20/2017 7:12:16 PM</span><span class="sxs-lookup"><span data-stu-id="07047-141">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB- Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : True EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 7:12:16 PM</span></span>

## <span data-ttu-id="07047-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07047-142">NOTES</span></span>

## <span data-ttu-id="07047-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07047-143">RELATED LINKS</span></span>

