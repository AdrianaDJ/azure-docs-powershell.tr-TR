---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 4fb10e2bb438cbc4f40936f9f9ead5c0bb36d861
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764515"
---
# <span data-ttu-id="cea4d-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="cea4d-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="cea4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea4d-102">SYNOPSIS</span></span>
<span data-ttu-id="cea4d-103">Belirtilen aboneliğin belirtilen kural açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cea4d-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cea4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cea4d-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cea4d-105">DESCRIPTION</span></span>
<span data-ttu-id="cea4d-106">**Set-AzureRmServiceBusRule** cmdlet 'i, verilen aboneliğin belirtilen kuralı için açıklama güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cea4d-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="cea4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cea4d-107">EXAMPLES</span></span>

### <span data-ttu-id="cea4d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cea4d-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="cea4d-109">Konudaki aboneliğin kuralındaki sqlexpression **mysqlexpression = ' Condition '** `SBEule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="cea4d-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="cea4d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cea4d-110">PARAMETERS</span></span>

### <span data-ttu-id="cea4d-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="cea4d-111">-Confirm</span></span>
<span data-ttu-id="cea4d-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cea4d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea4d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cea4d-113">-InputObject</span></span>
<span data-ttu-id="cea4d-114">ServiceBus kuralları tanımı.</span><span class="sxs-lookup"><span data-stu-id="cea4d-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cea4d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cea4d-115">-Name</span></span>
<span data-ttu-id="cea4d-116">Kural adı.</span><span class="sxs-lookup"><span data-stu-id="cea4d-116">Rule Name.</span></span>

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

### <span data-ttu-id="cea4d-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cea4d-117">-Namespace</span></span>
<span data-ttu-id="cea4d-118">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="cea4d-118">Namespace Name.</span></span>

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

### <span data-ttu-id="cea4d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea4d-119">-ResourceGroupName</span></span>
<span data-ttu-id="cea4d-120">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="cea4d-120">The name of the resource group</span></span>

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

### <span data-ttu-id="cea4d-121">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="cea4d-121">-Subscription</span></span>
<span data-ttu-id="cea4d-122">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="cea4d-122">Subscription Name.</span></span>

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

### <span data-ttu-id="cea4d-123">-Konu</span><span class="sxs-lookup"><span data-stu-id="cea4d-123">-Topic</span></span>
<span data-ttu-id="cea4d-124">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="cea4d-124">Topic Name.</span></span>

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

### <span data-ttu-id="cea4d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea4d-125">-WhatIf</span></span>
<span data-ttu-id="cea4d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cea4d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea4d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cea4d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea4d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea4d-128">-DefaultProfile</span></span>
<span data-ttu-id="cea4d-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cea4d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea4d-130">CommonParameters</span></span>
<span data-ttu-id="cea4d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cea4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea4d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea4d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea4d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cea4d-133">INPUTS</span></span>

### <span data-ttu-id="cea4d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cea4d-134">System.String</span></span>
<span data-ttu-id="cea4d-135">Microsoft. Azure. Commands. ServiceBus. modellerini. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="cea4d-135">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="cea4d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cea4d-136">OUTPUTS</span></span>

### <span data-ttu-id="cea4d-137">Microsoft. Azure. Commands. ServiceBus. modellerini. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="cea4d-137">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="cea4d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cea4d-138">NOTES</span></span>

## <span data-ttu-id="cea4d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cea4d-139">RELATED LINKS</span></span>

