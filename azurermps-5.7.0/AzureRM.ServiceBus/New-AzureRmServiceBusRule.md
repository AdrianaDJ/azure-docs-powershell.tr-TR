---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763219"
---
# <span data-ttu-id="b5d6c-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="b5d6c-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="b5d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d6c-103">Belirli bir konu aboneliği için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5d6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5d6c-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5d6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d6c-106">**Yeni-AzureRmServiceBusRule** cmdlet 'i, verilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="b5d6c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="b5d6c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5d6c-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="b5d6c-109">New-AzureRmServiceBusRule cmdlet 'i belirtilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="b5d6c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="b5d6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d6c-111">-DefaultProfile</span></span>
<span data-ttu-id="b5d6c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5d6c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5d6c-113">-Name</span></span>
<span data-ttu-id="b5d6c-114">Kural adı</span><span class="sxs-lookup"><span data-stu-id="b5d6c-114">Rule Name</span></span>

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

### <span data-ttu-id="b5d6c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b5d6c-115">-Namespace</span></span>
<span data-ttu-id="b5d6c-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-116">Namespace Name.</span></span>

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

### <span data-ttu-id="b5d6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5d6c-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b5d6c-118">The name of the resource group</span></span>

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

### <span data-ttu-id="b5d6c-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="b5d6c-119">-SqlExpression</span></span>
<span data-ttu-id="b5d6c-120">SQL Fillter Ifadesi</span><span class="sxs-lookup"><span data-stu-id="b5d6c-120">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="b5d6c-121">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="b5d6c-121">-Subscription</span></span>
<span data-ttu-id="b5d6c-122">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="b5d6c-122">Subscription Name</span></span>

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

### <span data-ttu-id="b5d6c-123">-Konu</span><span class="sxs-lookup"><span data-stu-id="b5d6c-123">-Topic</span></span>
<span data-ttu-id="b5d6c-124">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-124">Topic Name.</span></span>

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

### <span data-ttu-id="b5d6c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5d6c-125">-Confirm</span></span>
<span data-ttu-id="b5d6c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d6c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d6c-127">-WhatIf</span></span>
<span data-ttu-id="b5d6c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d6c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d6c-130">CommonParameters</span></span>
<span data-ttu-id="b5d6c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d6c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d6c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5d6c-133">INPUTS</span></span>

### <span data-ttu-id="b5d6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b5d6c-134">System.String</span></span>

## <span data-ttu-id="b5d6c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5d6c-135">OUTPUTS</span></span>

### <span data-ttu-id="b5d6c-136">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b5d6c-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="b5d6c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5d6c-137">NOTES</span></span>

## <span data-ttu-id="b5d6c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5d6c-138">RELATED LINKS</span></span>

