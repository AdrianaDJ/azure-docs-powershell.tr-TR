---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: cb6200156b68524119df86e24d812b97bcd250e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590023"
---
# <span data-ttu-id="d42ac-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="d42ac-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="d42ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d42ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d42ac-103">Belirtilen aboneliğin belirtilen kural açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d42ac-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d42ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d42ac-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d42ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d42ac-105">DESCRIPTION</span></span>
<span data-ttu-id="d42ac-106">**Set-AzureRmServiceBusRule** cmdlet 'i, verilen aboneliğin belirtilen kuralı için açıklama güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d42ac-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="d42ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d42ac-107">EXAMPLES</span></span>

### <span data-ttu-id="d42ac-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d42ac-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="d42ac-109">Konudaki aboneliğin kuralındaki sqlexpression **mysqlexpression = ' Condition '** `SBEule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="d42ac-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="d42ac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d42ac-110">PARAMETERS</span></span>

### <span data-ttu-id="d42ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42ac-111">-DefaultProfile</span></span>
<span data-ttu-id="d42ac-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d42ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d42ac-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d42ac-113">-InputObject</span></span>
<span data-ttu-id="d42ac-114">ServiceBus kuralları tanımı.</span><span class="sxs-lookup"><span data-stu-id="d42ac-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d42ac-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d42ac-115">-Name</span></span>
<span data-ttu-id="d42ac-116">Kural adı.</span><span class="sxs-lookup"><span data-stu-id="d42ac-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ac-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d42ac-117">-Namespace</span></span>
<span data-ttu-id="d42ac-118">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d42ac-118">Namespace Name.</span></span>

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

### <span data-ttu-id="d42ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d42ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="d42ac-120">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d42ac-120">The name of the resource group</span></span>

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

### <span data-ttu-id="d42ac-121">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="d42ac-121">-Subscription</span></span>
<span data-ttu-id="d42ac-122">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="d42ac-122">Subscription Name.</span></span>

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

### <span data-ttu-id="d42ac-123">-Konu</span><span class="sxs-lookup"><span data-stu-id="d42ac-123">-Topic</span></span>
<span data-ttu-id="d42ac-124">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="d42ac-124">Topic Name.</span></span>

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

### <span data-ttu-id="d42ac-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="d42ac-125">-Confirm</span></span>
<span data-ttu-id="d42ac-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d42ac-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ac-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d42ac-127">-WhatIf</span></span>
<span data-ttu-id="d42ac-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d42ac-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d42ac-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d42ac-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42ac-130">CommonParameters</span></span>
<span data-ttu-id="d42ac-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d42ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42ac-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d42ac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42ac-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d42ac-133">INPUTS</span></span>

### <span data-ttu-id="d42ac-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d42ac-134">System.String</span></span>

### <span data-ttu-id="d42ac-135">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d42ac-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="d42ac-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d42ac-136">OUTPUTS</span></span>

### <span data-ttu-id="d42ac-137">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d42ac-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="d42ac-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d42ac-138">NOTES</span></span>

## <span data-ttu-id="d42ac-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d42ac-139">RELATED LINKS</span></span>
