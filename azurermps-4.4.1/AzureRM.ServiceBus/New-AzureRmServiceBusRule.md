---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764771"
---
# <span data-ttu-id="607f2-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="607f2-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="607f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607f2-102">SYNOPSIS</span></span>
<span data-ttu-id="607f2-103">Belirli bir konu aboneliği için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="607f2-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="607f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="607f2-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="607f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="607f2-105">DESCRIPTION</span></span>
<span data-ttu-id="607f2-106">**Yeni-AzureRmServiceBusRule** cmdlet 'i, verilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="607f2-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="607f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="607f2-107">EXAMPLES</span></span>

### <span data-ttu-id="607f2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="607f2-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="607f2-109">**Yeni-AzureRmServiceBusRule** cmdlet 'ı belirtilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="607f2-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="607f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="607f2-110">PARAMETERS</span></span>

### <span data-ttu-id="607f2-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="607f2-111">-Confirm</span></span>
<span data-ttu-id="607f2-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="607f2-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607f2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="607f2-113">-Name</span></span>
<span data-ttu-id="607f2-114">Kural adı</span><span class="sxs-lookup"><span data-stu-id="607f2-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607f2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="607f2-115">-Namespace</span></span>
<span data-ttu-id="607f2-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="607f2-116">Namespace Name.</span></span>

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

### <span data-ttu-id="607f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="607f2-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="607f2-118">The name of the resource group</span></span>

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

### <span data-ttu-id="607f2-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="607f2-119">-SqlExpression</span></span>
<span data-ttu-id="607f2-120">SQL Fillter Ifadesi</span><span class="sxs-lookup"><span data-stu-id="607f2-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607f2-121">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="607f2-121">-Subscription</span></span>
<span data-ttu-id="607f2-122">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="607f2-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607f2-123">-Konu</span><span class="sxs-lookup"><span data-stu-id="607f2-123">-Topic</span></span>
<span data-ttu-id="607f2-124">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="607f2-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607f2-125">-WhatIf</span></span>
<span data-ttu-id="607f2-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="607f2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="607f2-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="607f2-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="607f2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="607f2-128">INPUTS</span></span>

### <span data-ttu-id="607f2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="607f2-129">System.String</span></span>


## <span data-ttu-id="607f2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="607f2-130">OUTPUTS</span></span>

### <span data-ttu-id="607f2-131">Microsoft. Azure. Commands. ServiceBus. modellerini. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="607f2-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="607f2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="607f2-132">NOTES</span></span>

## <span data-ttu-id="607f2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="607f2-133">RELATED LINKS</span></span>

