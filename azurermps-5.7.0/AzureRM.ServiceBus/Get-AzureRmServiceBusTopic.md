---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 56f41802687938bf7575049eadc59ab7b049ac2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763991"
---
# <span data-ttu-id="df1ac-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="df1ac-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="df1ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="df1ac-103">Belirtilen hizmet veri yolu konusu için bir açıklama döndürür.</span><span class="sxs-lookup"><span data-stu-id="df1ac-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df1ac-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df1ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df1ac-105">DESCRIPTION</span></span>
<span data-ttu-id="df1ac-106">**Get-AzureRmServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad alanı için bir konu açıklaması döndürür.</span><span class="sxs-lookup"><span data-stu-id="df1ac-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="df1ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df1ac-107">EXAMPLES</span></span>

### <span data-ttu-id="df1ac-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df1ac-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM
```
<span data-ttu-id="df1ac-109">Verilen hizmet veri yolu ad alanı için belirtilen konunun açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="df1ac-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="df1ac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df1ac-110">PARAMETERS</span></span>

### <span data-ttu-id="df1ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1ac-111">-DefaultProfile</span></span>
<span data-ttu-id="df1ac-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df1ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1ac-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="df1ac-113">-Name</span></span>
<span data-ttu-id="df1ac-114">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="df1ac-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1ac-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df1ac-115">-Namespace</span></span>
<span data-ttu-id="df1ac-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="df1ac-116">Namespace Name.</span></span>

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

### <span data-ttu-id="df1ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="df1ac-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="df1ac-118">The name of the resource group</span></span>

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

### <span data-ttu-id="df1ac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1ac-119">CommonParameters</span></span>
<span data-ttu-id="df1ac-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df1ac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1ac-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1ac-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1ac-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df1ac-122">INPUTS</span></span>

### <span data-ttu-id="df1ac-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df1ac-123">-ResourceGroup</span></span>
 <span data-ttu-id="df1ac-124">System. String</span><span class="sxs-lookup"><span data-stu-id="df1ac-124">System.String</span></span>
 

### <span data-ttu-id="df1ac-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="df1ac-125">-NamespaceName</span></span>
 <span data-ttu-id="df1ac-126">System. String</span><span class="sxs-lookup"><span data-stu-id="df1ac-126">System.String</span></span>
 

### <span data-ttu-id="df1ac-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="df1ac-127">-TopicName</span></span>
 <span data-ttu-id="df1ac-128">System. String</span><span class="sxs-lookup"><span data-stu-id="df1ac-128">System.String</span></span>

## <span data-ttu-id="df1ac-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df1ac-129">OUTPUTS</span></span>

### <span data-ttu-id="df1ac-130">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="df1ac-130">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="df1ac-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df1ac-131">NOTES</span></span>

## <span data-ttu-id="df1ac-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df1ac-132">RELATED LINKS</span></span>

