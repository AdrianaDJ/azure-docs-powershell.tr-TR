---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: df7cf094482f849782d6570b0df1af8cbadb7077
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759218"
---
# <span data-ttu-id="250d9-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="250d9-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="250d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="250d9-102">SYNOPSIS</span></span>
<span data-ttu-id="250d9-103">Verilen ad alanının NetworkRuleSet öğesine tek bir ıprule ekleme</span><span class="sxs-lookup"><span data-stu-id="250d9-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="250d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="250d9-104">SYNTAX</span></span>

### <span data-ttu-id="250d9-105">Iprulepropertiesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="250d9-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="250d9-106">Ipruleinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="250d9-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="250d9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="250d9-107">DESCRIPTION</span></span>
<span data-ttu-id="250d9-108">Verilen ad alanının NetworkRuleSet öğesine tek bir ıprule ekleme</span><span class="sxs-lookup"><span data-stu-id="250d9-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="250d9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="250d9-109">EXAMPLES</span></span>

### <span data-ttu-id="250d9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="250d9-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="250d9-111">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="250d9-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="250d9-112">ıprule 'i IPMask "11.22.33.44" ile ekleyin ve verilen ad sapce.</span><span class="sxs-lookup"><span data-stu-id="250d9-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

### <span data-ttu-id="250d9-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="250d9-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="250d9-114">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="250d9-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="250d9-115">ıprule 'i IPMask "11.22.33.44" ile ekleyin ve verilen ad sapce.</span><span class="sxs-lookup"><span data-stu-id="250d9-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

## <span data-ttu-id="250d9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="250d9-116">PARAMETERS</span></span>

### <span data-ttu-id="250d9-117">-Eylem</span><span class="sxs-lookup"><span data-stu-id="250d9-117">-Action</span></span>
<span data-ttu-id="250d9-118">IP filtre eylemi</span><span class="sxs-lookup"><span data-stu-id="250d9-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="250d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="250d9-119">-DefaultProfile</span></span>
<span data-ttu-id="250d9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="250d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="250d9-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="250d9-121">-IpMask</span></span>
<span data-ttu-id="250d9-122">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="250d9-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="250d9-123">-Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="250d9-123">-IpRuleObject</span></span>
<span data-ttu-id="250d9-124">Eklenecek ıprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="250d9-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="250d9-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="250d9-125">-Name</span></span>
<span data-ttu-id="250d9-126">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="250d9-126">Namespace Name</span></span>

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

### <span data-ttu-id="250d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="250d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="250d9-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="250d9-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="250d9-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="250d9-129">-Confirm</span></span>
<span data-ttu-id="250d9-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="250d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="250d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="250d9-131">-WhatIf</span></span>
<span data-ttu-id="250d9-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="250d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="250d9-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="250d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="250d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="250d9-134">CommonParameters</span></span>
<span data-ttu-id="250d9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="250d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="250d9-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="250d9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="250d9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="250d9-137">INPUTS</span></span>

### <span data-ttu-id="250d9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="250d9-138">System.String</span></span>

### <span data-ttu-id="250d9-139">Microsoft. Azure. Commands. ServiceBus. modeller. Psnwrulesetıprulesattributes</span><span class="sxs-lookup"><span data-stu-id="250d9-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="250d9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="250d9-140">OUTPUTS</span></span>

### <span data-ttu-id="250d9-141">Microsoft. Azure. Commands. ServiceBus. modeller. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="250d9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="250d9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="250d9-142">NOTES</span></span>

## <span data-ttu-id="250d9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="250d9-143">RELATED LINKS</span></span>