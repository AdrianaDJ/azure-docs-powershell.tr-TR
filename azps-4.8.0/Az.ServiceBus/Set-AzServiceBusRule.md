---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107604"
---
# <span data-ttu-id="26285-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="26285-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="26285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26285-102">SYNOPSIS</span></span>
<span data-ttu-id="26285-103">Belirtilen aboneliğin belirtilen kural açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26285-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="26285-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26285-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26285-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26285-105">DESCRIPTION</span></span>
<span data-ttu-id="26285-106">**Set-AzServiceBusRule** cmdlet 'i, verilen aboneliğin belirtilen kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26285-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="26285-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26285-107">EXAMPLES</span></span>

### <span data-ttu-id="26285-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26285-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="26285-109">Konudaki aboneliğin kuralındaki **mysqlexpression = ' Condition '** SQL ifadesini güncelleştirir `SBRule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="26285-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="26285-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26285-110">PARAMETERS</span></span>

### <span data-ttu-id="26285-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26285-111">-DefaultProfile</span></span>
<span data-ttu-id="26285-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26285-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26285-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26285-113">-InputObject</span></span>
<span data-ttu-id="26285-114">ServiceBus kuralları tanımı.</span><span class="sxs-lookup"><span data-stu-id="26285-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="26285-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="26285-115">-Name</span></span>
<span data-ttu-id="26285-116">Kural adı.</span><span class="sxs-lookup"><span data-stu-id="26285-116">Rule Name.</span></span>

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

### <span data-ttu-id="26285-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="26285-117">-Namespace</span></span>
<span data-ttu-id="26285-118">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="26285-118">Namespace Name.</span></span>

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

### <span data-ttu-id="26285-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26285-119">-ResourceGroupName</span></span>
<span data-ttu-id="26285-120">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="26285-120">The name of the resource group</span></span>

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

### <span data-ttu-id="26285-121">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="26285-121">-Subscription</span></span>
<span data-ttu-id="26285-122">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="26285-122">Subscription Name.</span></span>

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

### <span data-ttu-id="26285-123">-Konu</span><span class="sxs-lookup"><span data-stu-id="26285-123">-Topic</span></span>
<span data-ttu-id="26285-124">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="26285-124">Topic Name.</span></span>

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

### <span data-ttu-id="26285-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="26285-125">-Confirm</span></span>
<span data-ttu-id="26285-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26285-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26285-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26285-127">-WhatIf</span></span>
<span data-ttu-id="26285-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26285-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26285-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26285-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26285-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26285-130">CommonParameters</span></span>
<span data-ttu-id="26285-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26285-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26285-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26285-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26285-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26285-133">INPUTS</span></span>

### <span data-ttu-id="26285-134">System. String</span><span class="sxs-lookup"><span data-stu-id="26285-134">System.String</span></span>

### <span data-ttu-id="26285-135">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="26285-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="26285-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26285-136">OUTPUTS</span></span>

### <span data-ttu-id="26285-137">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="26285-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="26285-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26285-138">NOTES</span></span>

## <span data-ttu-id="26285-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26285-139">RELATED LINKS</span></span>
