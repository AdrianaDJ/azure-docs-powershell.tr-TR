---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 785685981c38248fba944cc9e3809a2de1f32e71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589677"
---
# <span data-ttu-id="a27df-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a27df-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="a27df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a27df-102">SYNOPSIS</span></span>
<span data-ttu-id="a27df-103">Belirtilen hizmet veri yolu ad alanındaki hizmet veri yolu sırasının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a27df-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a27df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a27df-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a27df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a27df-105">DESCRIPTION</span></span>
<span data-ttu-id="a27df-106">**Set-AzureRmServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki hizmet veri yolu sırasının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a27df-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a27df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a27df-107">EXAMPLES</span></span>

### <span data-ttu-id="a27df-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a27df-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:34 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 6:16:18 PM
```

<span data-ttu-id="a27df-109">Belirtilen sırayı belirtilen ad alanında yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a27df-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="a27df-110">Bu örnek **DeadLetteringOnMessageExpiration** özelliğini **true** ve **SupportOrdering** 'i **true** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a27df-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="a27df-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a27df-111">PARAMETERS</span></span>

### <span data-ttu-id="a27df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27df-112">-DefaultProfile</span></span>
<span data-ttu-id="a27df-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a27df-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a27df-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a27df-114">-InputObject</span></span>
<span data-ttu-id="a27df-115">ServiceBus tanımı.</span><span class="sxs-lookup"><span data-stu-id="a27df-115">ServiceBus definition.</span></span>

```yaml
Type: PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27df-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a27df-116">-Name</span></span>
<span data-ttu-id="a27df-117">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="a27df-117">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27df-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a27df-118">-Namespace</span></span>
<span data-ttu-id="a27df-119">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a27df-119">Namespace Name.</span></span>

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

### <span data-ttu-id="a27df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27df-120">-ResourceGroupName</span></span>
<span data-ttu-id="a27df-121">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a27df-121">The name of the resource group</span></span>

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

### <span data-ttu-id="a27df-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a27df-122">-Confirm</span></span>
<span data-ttu-id="a27df-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a27df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a27df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a27df-124">-WhatIf</span></span>
<span data-ttu-id="a27df-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a27df-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a27df-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a27df-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a27df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27df-127">CommonParameters</span></span>
<span data-ttu-id="a27df-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a27df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27df-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a27df-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27df-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a27df-130">INPUTS</span></span>

### <span data-ttu-id="a27df-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a27df-131">-ResourceGroup</span></span>
 <span data-ttu-id="a27df-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a27df-132">System.String</span></span>

### <span data-ttu-id="a27df-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a27df-133">-NamespaceName</span></span>
 <span data-ttu-id="a27df-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a27df-134">System.String</span></span>

### <span data-ttu-id="a27df-135">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="a27df-135">-QueueName</span></span>
 <span data-ttu-id="a27df-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a27df-136">System.String</span></span>

### <span data-ttu-id="a27df-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="a27df-137">-QueueObj</span></span>
 <span data-ttu-id="a27df-138">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="a27df-138">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="a27df-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a27df-139">OUTPUTS</span></span>

### <span data-ttu-id="a27df-140">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="a27df-140">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="a27df-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a27df-141">NOTES</span></span>

## <span data-ttu-id="a27df-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a27df-142">RELATED LINKS</span></span>

