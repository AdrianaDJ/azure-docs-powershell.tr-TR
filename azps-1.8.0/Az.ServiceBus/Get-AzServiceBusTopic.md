---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: ff3ab640de435898f665f0994a63f904decda5cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759193"
---
# <span data-ttu-id="2a5fa-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="2a5fa-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="2a5fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5fa-103">Belirtilen hizmet veri yolu konusu için bir açıklama döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="2a5fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a5fa-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a5fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="2a5fa-106">**Get-AzServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanı için bir konu açıklaması döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2a5fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a5fa-107">EXAMPLES</span></span>

### <span data-ttu-id="2a5fa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a5fa-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="2a5fa-109">Verilen hizmet veri yolu ad alanı için belirtilen konunun açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="2a5fa-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2a5fa-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="2a5fa-111">Verilen hizmet veri yolu ad alanı için konu listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="2a5fa-112">Varsayılan olarak, 100 konu başlığı altında en fazla 100 konu döndürülürse, lütfen-MaxCount parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="2a5fa-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2a5fa-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="2a5fa-114">Verilen hizmet veri yolu ad alanı için ilk 150 konularının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="2a5fa-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a5fa-115">PARAMETERS</span></span>

### <span data-ttu-id="2a5fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5fa-116">-DefaultProfile</span></span>
<span data-ttu-id="2a5fa-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a5fa-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2a5fa-118">-MaxCount</span></span>
<span data-ttu-id="2a5fa-119">Döndürülecek en fazla konu sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-119">Determine the maximum number of Topics to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5fa-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a5fa-120">-Name</span></span>
<span data-ttu-id="2a5fa-121">Konu adı</span><span class="sxs-lookup"><span data-stu-id="2a5fa-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5fa-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2a5fa-122">-Namespace</span></span>
<span data-ttu-id="2a5fa-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="2a5fa-123">Namespace Name</span></span>

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

### <span data-ttu-id="2a5fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a5fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a5fa-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2a5fa-125">The name of the resource group</span></span>

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

### <span data-ttu-id="2a5fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5fa-126">CommonParameters</span></span>
<span data-ttu-id="2a5fa-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a5fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5fa-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a5fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5fa-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a5fa-129">INPUTS</span></span>

### <span data-ttu-id="2a5fa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2a5fa-130">System.String</span></span>

## <span data-ttu-id="2a5fa-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a5fa-131">OUTPUTS</span></span>

### <span data-ttu-id="2a5fa-132">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="2a5fa-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2a5fa-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a5fa-133">NOTES</span></span>

## <span data-ttu-id="2a5fa-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a5fa-134">RELATED LINKS</span></span>