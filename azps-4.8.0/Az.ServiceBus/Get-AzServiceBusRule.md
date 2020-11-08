---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0f765f8cf59453ee8b89317da2fa123785ee7f90
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107617"
---
# <span data-ttu-id="0f715-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="0f715-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="0f715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f715-102">SYNOPSIS</span></span>
<span data-ttu-id="0f715-103">Verilen bir konu aboneliğindeki mevcut bir kuralın tanımını getirir.</span><span class="sxs-lookup"><span data-stu-id="0f715-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="0f715-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f715-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f715-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f715-105">DESCRIPTION</span></span>
<span data-ttu-id="0f715-106">**Get-AzServiceBusRule** cmdlet 'i, belirtilen kuralın söz konusu aboneliğindeki açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="0f715-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="0f715-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f715-107">EXAMPLES</span></span>

### <span data-ttu-id="0f715-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0f715-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="0f715-109">Belirtilen aboneliğin belirtilen kural açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f715-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="0f715-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0f715-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="0f715-111">Belirtilen aboneliğin kural açıklamaları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f715-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="0f715-112">Varsayılan olarak 100 kuralı döndürülecek, 100 taneden fazla kural döndürülürse, lütfen-MaxCount parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0f715-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="0f715-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0f715-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="0f715-114">Belirtilen bir aboneliğin ilk 150 kuralı açıklamalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f715-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="0f715-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f715-115">PARAMETERS</span></span>

### <span data-ttu-id="0f715-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f715-116">-DefaultProfile</span></span>
<span data-ttu-id="0f715-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f715-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f715-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0f715-118">-MaxCount</span></span>
<span data-ttu-id="0f715-119">Döndürülecek kural sayısının üst sınırını belirleme.</span><span class="sxs-lookup"><span data-stu-id="0f715-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="0f715-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f715-120">-Name</span></span>
<span data-ttu-id="0f715-121">Kural adı</span><span class="sxs-lookup"><span data-stu-id="0f715-121">Rule Name</span></span>

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

### <span data-ttu-id="0f715-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0f715-122">-Namespace</span></span>
<span data-ttu-id="0f715-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="0f715-123">Namespace Name</span></span>

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

### <span data-ttu-id="0f715-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f715-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f715-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0f715-125">The name of the resource group</span></span>

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

### <span data-ttu-id="0f715-126">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="0f715-126">-Subscription</span></span>
<span data-ttu-id="0f715-127">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="0f715-127">Subscription Name</span></span>

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

### <span data-ttu-id="0f715-128">-Konu</span><span class="sxs-lookup"><span data-stu-id="0f715-128">-Topic</span></span>
<span data-ttu-id="0f715-129">Konu adı</span><span class="sxs-lookup"><span data-stu-id="0f715-129">Topic Name</span></span>

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

### <span data-ttu-id="0f715-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f715-130">CommonParameters</span></span>
<span data-ttu-id="0f715-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f715-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f715-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f715-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f715-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f715-133">INPUTS</span></span>

### <span data-ttu-id="0f715-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0f715-134">System.String</span></span>

## <span data-ttu-id="0f715-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f715-135">OUTPUTS</span></span>

### <span data-ttu-id="0f715-136">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0f715-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="0f715-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f715-137">NOTES</span></span>

## <span data-ttu-id="0f715-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f715-138">RELATED LINKS</span></span>
