---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: ddccdb907dac89466a81be62e104202a3e59a672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592732"
---
# <span data-ttu-id="005c6-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="005c6-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="005c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="005c6-102">SYNOPSIS</span></span>
<span data-ttu-id="005c6-103">Belirtilen hizmet veri yolu konusu için bir açıklama döndürür.</span><span class="sxs-lookup"><span data-stu-id="005c6-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="005c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="005c6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="005c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="005c6-105">DESCRIPTION</span></span>
<span data-ttu-id="005c6-106">**Get-AzureRmServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanı için bir konu açıklaması döndürür.</span><span class="sxs-lookup"><span data-stu-id="005c6-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="005c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="005c6-107">EXAMPLES</span></span>

### <span data-ttu-id="005c6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="005c6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

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

<span data-ttu-id="005c6-109">Verilen hizmet veri yolu ad alanı için belirtilen konunun açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="005c6-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="005c6-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="005c6-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="005c6-111">Verilen hizmet veri yolu ad alanı için konu listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="005c6-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="005c6-112">Varsayılan olarak, 100 konu başlığı altında en fazla 100 konu döndürülürse, lütfen-MaxCount parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="005c6-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="005c6-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="005c6-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="005c6-114">Verilen hizmet veri yolu ad alanı için ilk 150 konularının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="005c6-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="005c6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="005c6-115">PARAMETERS</span></span>

### <span data-ttu-id="005c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="005c6-116">-DefaultProfile</span></span>
<span data-ttu-id="005c6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="005c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="005c6-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="005c6-118">-MaxCount</span></span>
<span data-ttu-id="005c6-119">Döndürülecek en fazla konu sayısını belirleme.</span><span class="sxs-lookup"><span data-stu-id="005c6-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="005c6-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="005c6-120">-Name</span></span>
<span data-ttu-id="005c6-121">Konu adı</span><span class="sxs-lookup"><span data-stu-id="005c6-121">Topic Name</span></span>

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

### <span data-ttu-id="005c6-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="005c6-122">-Namespace</span></span>
<span data-ttu-id="005c6-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="005c6-123">Namespace Name</span></span>

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

### <span data-ttu-id="005c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="005c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="005c6-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="005c6-125">The name of the resource group</span></span>

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

### <span data-ttu-id="005c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="005c6-126">CommonParameters</span></span>
<span data-ttu-id="005c6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="005c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="005c6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="005c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="005c6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="005c6-129">INPUTS</span></span>

### <span data-ttu-id="005c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="005c6-130">System.String</span></span>

## <span data-ttu-id="005c6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="005c6-131">OUTPUTS</span></span>

### <span data-ttu-id="005c6-132">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="005c6-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="005c6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="005c6-133">NOTES</span></span>

## <span data-ttu-id="005c6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="005c6-134">RELATED LINKS</span></span>