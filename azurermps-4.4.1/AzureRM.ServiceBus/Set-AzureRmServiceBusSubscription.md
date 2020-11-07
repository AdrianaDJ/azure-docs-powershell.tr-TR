---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764514"
---
# <span data-ttu-id="dfb1c-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="dfb1c-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="dfb1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb1c-103">Belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun abonelik açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfb1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfb1c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfb1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfb1c-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb1c-106">**Set-AzureRmServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki hizmet veri yolu konusunun aboneliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dfb1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfb1c-107">EXAMPLES</span></span>

### <span data-ttu-id="dfb1c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dfb1c-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="dfb1c-109">Belirtilen aboneliğin açıklamasını verilen konuya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="dfb1c-110">Bu örnek, **DeadLetteringOnMessageExpiration** özelliğini **true** ve **maxdeliverycount** 'ı 9 olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="dfb1c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfb1c-111">PARAMETERS</span></span>

### <span data-ttu-id="dfb1c-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="dfb1c-112">-Confirm</span></span>
<span data-ttu-id="dfb1c-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb1c-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb1c-114">-WhatIf</span></span>
<span data-ttu-id="dfb1c-115">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb1c-116">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb1c-117">-DefaultProfile</span></span>
<span data-ttu-id="dfb1c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfb1c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfb1c-119">-InputObject</span></span>
<span data-ttu-id="dfb1c-120">ServiceBus abonelik tanımı.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb1c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dfb1c-121">-Namespace</span></span>
<span data-ttu-id="dfb1c-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-122">Namespace Name.</span></span>

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

### <span data-ttu-id="dfb1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfb1c-124">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="dfb1c-124">The name of the resource group</span></span>

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

### <span data-ttu-id="dfb1c-125">-Konu</span><span class="sxs-lookup"><span data-stu-id="dfb1c-125">-Topic</span></span>
<span data-ttu-id="dfb1c-126">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-126">Topic Name.</span></span>

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

### <span data-ttu-id="dfb1c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb1c-127">CommonParameters</span></span>
<span data-ttu-id="dfb1c-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfb1c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb1c-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb1c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb1c-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfb1c-130">INPUTS</span></span>

### <span data-ttu-id="dfb1c-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dfb1c-131">-ResourceGroup</span></span>
 <span data-ttu-id="dfb1c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb1c-132">System.String</span></span>

### <span data-ttu-id="dfb1c-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="dfb1c-133">-NamespaceName</span></span>
 <span data-ttu-id="dfb1c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb1c-134">System.String</span></span>

### <span data-ttu-id="dfb1c-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="dfb1c-135">-TopicName</span></span>
 <span data-ttu-id="dfb1c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb1c-136">System.String</span></span>

### <span data-ttu-id="dfb1c-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="dfb1c-137">-SubscriptionObj</span></span>
 <span data-ttu-id="dfb1c-138">Microsoft. Azure. Commands. ServiceBus. model. Subscriptionöznitelikleri</span><span class="sxs-lookup"><span data-stu-id="dfb1c-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="dfb1c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfb1c-139">OUTPUTS</span></span>

### <span data-ttu-id="dfb1c-140">Microsoft. Azure. Commands. ServiceBus. model. Subscriptionöznitelikleri</span><span class="sxs-lookup"><span data-stu-id="dfb1c-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="dfb1c-141">Ad: SB-TopicSubscription-example1 konumu: Batı US AccessedAt: 1/1/0001 12:00:00 Ao Autodeleteonıdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 PM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: true EnableBatchedOperations: true EntityAvailabilityStatus: kullanılabilir IsReadOnly: LockDuration: 00:01:00 maxdeliverycount: 1/20/2017 9:59:15</span><span class="sxs-lookup"><span data-stu-id="dfb1c-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="dfb1c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfb1c-142">NOTES</span></span>

## <span data-ttu-id="dfb1c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfb1c-143">RELATED LINKS</span></span>

