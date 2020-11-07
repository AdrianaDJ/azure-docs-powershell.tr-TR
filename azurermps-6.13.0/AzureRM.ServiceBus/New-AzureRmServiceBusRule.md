---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 6ef5b99f916724dcdb746d67a6f9373e4bbfc9ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762893"
---
# <span data-ttu-id="4655b-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4655b-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="4655b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4655b-102">SYNOPSIS</span></span>
<span data-ttu-id="4655b-103">Belirli bir konu aboneliği için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4655b-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4655b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4655b-104">SYNTAX</span></span>

### <span data-ttu-id="4655b-105">RulePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4655b-105">RulePropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655b-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="4655b-106">RuleActionPropertiesSet</span></span>
```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4655b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4655b-107">DESCRIPTION</span></span>
<span data-ttu-id="4655b-108">**Yeni-AzureRmServiceBusRule** cmdlet 'i, verilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4655b-108">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="4655b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4655b-109">EXAMPLES</span></span>

### <span data-ttu-id="4655b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4655b-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="4655b-111">New-AzureRmServiceBusRule cmdlet 'i belirtilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4655b-111">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>


### <span data-ttu-id="4655b-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4655b-112">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="4655b-113">New-AzureRmServiceBusRule cmdlet 'i, ActionFilter ile belirtilen abonelik için yeni bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4655b-113">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="4655b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4655b-114">PARAMETERS</span></span>

### <span data-ttu-id="4655b-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="4655b-115">-ActionSqlExpression</span></span>
<span data-ttu-id="4655b-116">Eylem SqlFillter Ifadesi</span><span class="sxs-lookup"><span data-stu-id="4655b-116">Action SqlFillter Expression</span></span>

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

### <span data-ttu-id="4655b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4655b-117">-DefaultProfile</span></span>
<span data-ttu-id="4655b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4655b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4655b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="4655b-119">-Name</span></span>
<span data-ttu-id="4655b-120">Kural adı</span><span class="sxs-lookup"><span data-stu-id="4655b-120">Rule Name</span></span>

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

### <span data-ttu-id="4655b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4655b-121">-Namespace</span></span>
<span data-ttu-id="4655b-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="4655b-122">Namespace Name</span></span>

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

### <span data-ttu-id="4655b-123">-Requiresönişleme</span><span class="sxs-lookup"><span data-stu-id="4655b-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="4655b-124">Eylem Için ön Işleme gerekir</span><span class="sxs-lookup"><span data-stu-id="4655b-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="4655b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4655b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4655b-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4655b-126">The name of the resource group</span></span>

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

### <span data-ttu-id="4655b-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="4655b-127">-SqlExpression</span></span>
<span data-ttu-id="4655b-128">SQL Fillter Ifadesi</span><span class="sxs-lookup"><span data-stu-id="4655b-128">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="4655b-129">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="4655b-129">-Subscription</span></span>
<span data-ttu-id="4655b-130">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="4655b-130">Subscription Name</span></span>

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

### <span data-ttu-id="4655b-131">-Konu</span><span class="sxs-lookup"><span data-stu-id="4655b-131">-Topic</span></span>
<span data-ttu-id="4655b-132">Konu adı</span><span class="sxs-lookup"><span data-stu-id="4655b-132">Topic Name</span></span>

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

### <span data-ttu-id="4655b-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="4655b-133">-Confirm</span></span>
<span data-ttu-id="4655b-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4655b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4655b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4655b-135">-WhatIf</span></span>
<span data-ttu-id="4655b-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4655b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4655b-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4655b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4655b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4655b-138">CommonParameters</span></span>
<span data-ttu-id="4655b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4655b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4655b-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4655b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4655b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4655b-141">INPUTS</span></span>

### <span data-ttu-id="4655b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4655b-142">System.String</span></span>


## <span data-ttu-id="4655b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4655b-143">OUTPUTS</span></span>

### <span data-ttu-id="4655b-144">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="4655b-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>


## <span data-ttu-id="4655b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4655b-145">NOTES</span></span>

## <span data-ttu-id="4655b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4655b-146">RELATED LINKS</span></span>