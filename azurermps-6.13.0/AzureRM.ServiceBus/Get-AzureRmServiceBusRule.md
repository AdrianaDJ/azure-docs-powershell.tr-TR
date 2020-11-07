---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 2d249d8935b79c310e4ca0aa1270ee67bf33ece3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762899"
---
# <span data-ttu-id="3366a-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="3366a-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="3366a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3366a-102">SYNOPSIS</span></span>
<span data-ttu-id="3366a-103">Belirli bir konu aboneliği için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3366a-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3366a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3366a-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3366a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3366a-105">DESCRIPTION</span></span>
<span data-ttu-id="3366a-106">**Get-AzureRmServiceBusRule** cmdlet 'i belirtilen kuralın söz konusu aboneliğindeki açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="3366a-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="3366a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3366a-107">EXAMPLES</span></span>

### <span data-ttu-id="3366a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3366a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="3366a-109">Belirtilen aboneliğin belirtilen kural açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="3366a-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="3366a-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3366a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="3366a-111">Belirtilen aboneliğin kural açıklamaları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3366a-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="3366a-112">Varsayılan olarak 100 kuralı döndürülecek, 100 taneden fazla kural döndürülürse, lütfen-MaxCount parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3366a-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="3366a-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3366a-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="3366a-114">Belirtilen bir aboneliğin ilk 150 kuralı açıklamalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3366a-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="3366a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3366a-115">PARAMETERS</span></span>

### <span data-ttu-id="3366a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3366a-116">-DefaultProfile</span></span>
<span data-ttu-id="3366a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3366a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3366a-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3366a-118">-MaxCount</span></span>
<span data-ttu-id="3366a-119">Döndürülecek kural sayısının üst sınırını belirleme.</span><span class="sxs-lookup"><span data-stu-id="3366a-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="3366a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3366a-120">-Name</span></span>
<span data-ttu-id="3366a-121">Kural adı</span><span class="sxs-lookup"><span data-stu-id="3366a-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3366a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3366a-122">-Namespace</span></span>
<span data-ttu-id="3366a-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="3366a-123">Namespace Name</span></span>

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

### <span data-ttu-id="3366a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3366a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3366a-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3366a-125">The name of the resource group</span></span>

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

### <span data-ttu-id="3366a-126">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="3366a-126">-Subscription</span></span>
<span data-ttu-id="3366a-127">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="3366a-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3366a-128">-Konu</span><span class="sxs-lookup"><span data-stu-id="3366a-128">-Topic</span></span>
<span data-ttu-id="3366a-129">Konu adı</span><span class="sxs-lookup"><span data-stu-id="3366a-129">Topic Name</span></span>

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

### <span data-ttu-id="3366a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3366a-130">CommonParameters</span></span>
<span data-ttu-id="3366a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3366a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3366a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3366a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3366a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3366a-133">INPUTS</span></span>

### <span data-ttu-id="3366a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3366a-134">System.String</span></span>

## <span data-ttu-id="3366a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3366a-135">OUTPUTS</span></span>

### <span data-ttu-id="3366a-136">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3366a-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="3366a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3366a-137">NOTES</span></span>

## <span data-ttu-id="3366a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3366a-138">RELATED LINKS</span></span>
