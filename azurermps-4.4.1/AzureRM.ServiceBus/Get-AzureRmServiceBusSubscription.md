---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587791"
---
# <span data-ttu-id="ed8df-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ed8df-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="ed8df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8df-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8df-103">Belirtilen konu için abonelik açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed8df-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed8df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed8df-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed8df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed8df-105">DESCRIPTION</span></span>
<span data-ttu-id="ed8df-106">**Get-AzureRmServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu konusu için abonelik açıklaması döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed8df-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="ed8df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed8df-107">EXAMPLES</span></span>

### <span data-ttu-id="ed8df-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed8df-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="ed8df-109">Belirtilen hizmet veri yolu konusu için abonelik açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed8df-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="ed8df-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed8df-110">PARAMETERS</span></span>

### <span data-ttu-id="ed8df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8df-111">-DefaultProfile</span></span>
<span data-ttu-id="ed8df-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed8df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed8df-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed8df-113">-Name</span></span>
<span data-ttu-id="ed8df-114">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="ed8df-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8df-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ed8df-115">-Namespace</span></span>
<span data-ttu-id="ed8df-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ed8df-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ed8df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8df-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed8df-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ed8df-118">The name of the resource group</span></span>

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

### <span data-ttu-id="ed8df-119">-Konu</span><span class="sxs-lookup"><span data-stu-id="ed8df-119">-Topic</span></span>
<span data-ttu-id="ed8df-120">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="ed8df-120">Topic Name.</span></span>

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

### <span data-ttu-id="ed8df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8df-121">CommonParameters</span></span>
<span data-ttu-id="ed8df-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed8df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8df-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8df-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8df-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed8df-124">INPUTS</span></span>

### <span data-ttu-id="ed8df-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed8df-125">-ResourceGroup</span></span>
 <span data-ttu-id="ed8df-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8df-126">System.String</span></span>
 

### <span data-ttu-id="ed8df-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ed8df-127">-NamespaceName</span></span>
 <span data-ttu-id="ed8df-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8df-128">System.String</span></span>
 

### <span data-ttu-id="ed8df-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ed8df-129">-TopicName</span></span>
 <span data-ttu-id="ed8df-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8df-130">System.String</span></span>
 

### <span data-ttu-id="ed8df-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ed8df-131">-SubscriptionName</span></span>
 <span data-ttu-id="ed8df-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8df-132">System.String</span></span>
 

## <span data-ttu-id="ed8df-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed8df-133">OUTPUTS</span></span>

### <span data-ttu-id="ed8df-134">Microsoft. Azure. Commands. ServiceBus. model. Subscriptionöznitelikleri</span><span class="sxs-lookup"><span data-stu-id="ed8df-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="ed8df-135">Ad: SB-TopicSubscription-example1 konumu: Batı US AccessedAt: 1/20/2017 3:18:54 har Autodeleteıdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. modeller. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 ısdefaultmessagetimetolive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus:. 1/20/2017 3:18:54 00:01:00</span><span class="sxs-lookup"><span data-stu-id="ed8df-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="ed8df-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed8df-136">NOTES</span></span>

## <span data-ttu-id="ed8df-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed8df-137">RELATED LINKS</span></span>

