---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588759"
---
# <span data-ttu-id="df6c3-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="df6c3-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="df6c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="df6c3-103">Belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="df6c3-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df6c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df6c3-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df6c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df6c3-105">DESCRIPTION</span></span>
<span data-ttu-id="df6c3-106">**Set-AzureRmServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun açıklama nesnesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="df6c3-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="df6c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df6c3-107">EXAMPLES</span></span>

### <span data-ttu-id="df6c3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df6c3-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="df6c3-109">Belirtilen konuyu belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="df6c3-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="df6c3-110">Bu örnek, **Enableexpress** özelliğini **doğru** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="df6c3-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="df6c3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df6c3-111">PARAMETERS</span></span>

### <span data-ttu-id="df6c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6c3-112">-DefaultProfile</span></span>
<span data-ttu-id="df6c3-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df6c3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6c3-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df6c3-114">-InputObject</span></span>
<span data-ttu-id="df6c3-115">ServiceBus konu tanımı.</span><span class="sxs-lookup"><span data-stu-id="df6c3-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6c3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="df6c3-116">-Name</span></span>
<span data-ttu-id="df6c3-117">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="df6c3-117">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6c3-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df6c3-118">-Namespace</span></span>
<span data-ttu-id="df6c3-119">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="df6c3-119">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6c3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df6c3-120">-ResourceGroupName</span></span>
<span data-ttu-id="df6c3-121">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="df6c3-121">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6c3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="df6c3-122">-Confirm</span></span>
<span data-ttu-id="df6c3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df6c3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6c3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df6c3-124">-WhatIf</span></span>
<span data-ttu-id="df6c3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df6c3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df6c3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df6c3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6c3-127">CommonParameters</span></span>
<span data-ttu-id="df6c3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df6c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6c3-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6c3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6c3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df6c3-130">INPUTS</span></span>

### <span data-ttu-id="df6c3-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df6c3-131">-ResourceGroup</span></span>
 <span data-ttu-id="df6c3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="df6c3-132">System.String</span></span>

### <span data-ttu-id="df6c3-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="df6c3-133">-NamespaceName</span></span>
 <span data-ttu-id="df6c3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="df6c3-134">System.String</span></span>

### <span data-ttu-id="df6c3-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="df6c3-135">-TopicName</span></span>
 <span data-ttu-id="df6c3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="df6c3-136">System.String</span></span>

### <span data-ttu-id="df6c3-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="df6c3-137">-TopicObj</span></span>
 <span data-ttu-id="df6c3-138">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="df6c3-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="df6c3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df6c3-139">OUTPUTS</span></span>

### <span data-ttu-id="df6c3-140">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="df6c3-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="df6c3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df6c3-141">NOTES</span></span>

## <span data-ttu-id="df6c3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df6c3-142">RELATED LINKS</span></span>

