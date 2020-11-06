---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: dbc3acdf65f97e5fa46d9359f1f7af43c2c137d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590861"
---
# <span data-ttu-id="4e57d-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4e57d-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="4e57d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e57d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e57d-103">Belirtilen hizmet veri yolu ad alanındaki bir hizmet veri yolu konusunun abonelik açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e57d-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e57d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e57d-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e57d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e57d-105">DESCRIPTION</span></span>
<span data-ttu-id="4e57d-106">**Set-AzureRmServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki hizmet veri yolu konusunun aboneliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e57d-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4e57d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e57d-107">EXAMPLES</span></span>

### <span data-ttu-id="4e57d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4e57d-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="4e57d-109">Belirtilen aboneliğin açıklamasını verilen konuya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e57d-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="4e57d-110">Bu örnek, **DeadLetteringOnMessageExpiration** özelliğini **true** ve **maxdeliverycount** 'ı 9 olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e57d-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="4e57d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e57d-111">PARAMETERS</span></span>

### <span data-ttu-id="4e57d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e57d-112">-DefaultProfile</span></span>
<span data-ttu-id="4e57d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e57d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e57d-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e57d-114">-InputObject</span></span>
<span data-ttu-id="4e57d-115">ServiceBus abonelik tanımı.</span><span class="sxs-lookup"><span data-stu-id="4e57d-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e57d-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e57d-116">-Namespace</span></span>
<span data-ttu-id="4e57d-117">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="4e57d-117">Namespace Name.</span></span>

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

### <span data-ttu-id="4e57d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e57d-118">-ResourceGroupName</span></span>
<span data-ttu-id="4e57d-119">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4e57d-119">The name of the resource group</span></span>

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

### <span data-ttu-id="4e57d-120">-Konu</span><span class="sxs-lookup"><span data-stu-id="4e57d-120">-Topic</span></span>
<span data-ttu-id="4e57d-121">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="4e57d-121">Topic Name.</span></span>

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

### <span data-ttu-id="4e57d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e57d-122">-Confirm</span></span>
<span data-ttu-id="4e57d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e57d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e57d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e57d-124">-WhatIf</span></span>
<span data-ttu-id="4e57d-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e57d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e57d-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e57d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e57d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e57d-127">CommonParameters</span></span>
<span data-ttu-id="4e57d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e57d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e57d-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e57d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e57d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e57d-130">INPUTS</span></span>

### <span data-ttu-id="4e57d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4e57d-131">System.String</span></span>

### <span data-ttu-id="4e57d-132">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4e57d-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="4e57d-133">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e57d-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4e57d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e57d-134">OUTPUTS</span></span>

### <span data-ttu-id="4e57d-135">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4e57d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="4e57d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e57d-136">NOTES</span></span>

## <span data-ttu-id="4e57d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e57d-137">RELATED LINKS</span></span>
