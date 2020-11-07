---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 869bfdaa7ff772980b7acf1caee6c7d6a8784d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759180"
---
# <span data-ttu-id="5196d-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="5196d-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="5196d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5196d-102">SYNOPSIS</span></span>
<span data-ttu-id="5196d-103">Belirli bir konu aboneliği için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5196d-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="5196d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5196d-104">SYNTAX</span></span>

### <span data-ttu-id="5196d-105">RulePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5196d-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5196d-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="5196d-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5196d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5196d-107">DESCRIPTION</span></span>
<span data-ttu-id="5196d-108">**New-AzServiceBusRule** cmdlet 'i, verilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5196d-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="5196d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5196d-109">EXAMPLES</span></span>

### <span data-ttu-id="5196d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5196d-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="5196d-111">New-AzServiceBusRule cmdlet 'i belirtilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5196d-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="5196d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5196d-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="5196d-113">New-AzServiceBusRule cmdlet 'i, ActionFilter ile belirtilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5196d-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="5196d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5196d-114">PARAMETERS</span></span>

### <span data-ttu-id="5196d-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="5196d-115">-ActionSqlExpression</span></span>
<span data-ttu-id="5196d-116">Eylem SqlFillter Ifadesi</span><span class="sxs-lookup"><span data-stu-id="5196d-116">Action SqlFillter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5196d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5196d-117">-DefaultProfile</span></span>
<span data-ttu-id="5196d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5196d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5196d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5196d-119">-Name</span></span>
<span data-ttu-id="5196d-120">Kural adı</span><span class="sxs-lookup"><span data-stu-id="5196d-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5196d-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5196d-121">-Namespace</span></span>
<span data-ttu-id="5196d-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="5196d-122">Namespace Name</span></span>

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

### <span data-ttu-id="5196d-123">-Requiresönişleme</span><span class="sxs-lookup"><span data-stu-id="5196d-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="5196d-124">Eylem Için ön Işleme gerekir</span><span class="sxs-lookup"><span data-stu-id="5196d-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5196d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5196d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5196d-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5196d-126">The name of the resource group</span></span>

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

### <span data-ttu-id="5196d-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="5196d-127">-SqlExpression</span></span>
<span data-ttu-id="5196d-128">SQL Fillter Ifadesi</span><span class="sxs-lookup"><span data-stu-id="5196d-128">Sql Fillter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5196d-129">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="5196d-129">-Subscription</span></span>
<span data-ttu-id="5196d-130">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="5196d-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5196d-131">-Konu</span><span class="sxs-lookup"><span data-stu-id="5196d-131">-Topic</span></span>
<span data-ttu-id="5196d-132">Konu adı</span><span class="sxs-lookup"><span data-stu-id="5196d-132">Topic Name</span></span>

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

### <span data-ttu-id="5196d-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="5196d-133">-Confirm</span></span>
<span data-ttu-id="5196d-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5196d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5196d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5196d-135">-WhatIf</span></span>
<span data-ttu-id="5196d-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5196d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5196d-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5196d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5196d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5196d-138">CommonParameters</span></span>
<span data-ttu-id="5196d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5196d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5196d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5196d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5196d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5196d-141">INPUTS</span></span>

### <span data-ttu-id="5196d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5196d-142">System.String</span></span>

## <span data-ttu-id="5196d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5196d-143">OUTPUTS</span></span>

### <span data-ttu-id="5196d-144">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="5196d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="5196d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5196d-145">NOTES</span></span>

## <span data-ttu-id="5196d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5196d-146">RELATED LINKS</span></span>