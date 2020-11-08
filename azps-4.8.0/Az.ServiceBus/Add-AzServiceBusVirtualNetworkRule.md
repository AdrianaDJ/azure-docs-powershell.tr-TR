---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 3ff1f64bf65a4474dc9f47aa6bd419c442b49698
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108741"
---
# <span data-ttu-id="fc5da-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fc5da-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="fc5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc5da-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5da-103">Verilen ad alanı için NetworkRuleSet 'e tek VirtualNetworkRule ekleme</span><span class="sxs-lookup"><span data-stu-id="fc5da-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="fc5da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc5da-104">SYNTAX</span></span>

### <span data-ttu-id="fc5da-105">VirtualNetworkRulePropertiesParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc5da-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc5da-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc5da-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc5da-107">DESCRIPTION</span></span>
<span data-ttu-id="fc5da-108">Verilen ad alanı için NetworkRuleSet 'e tek VirtualNetworkRule ekleme</span><span class="sxs-lookup"><span data-stu-id="fc5da-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="fc5da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc5da-109">EXAMPLES</span></span>

### <span data-ttu-id="fc5da-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc5da-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="fc5da-111">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="fc5da-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="fc5da-112">Verilen alt ağ ve ıgnoremissingvnetserviceendpoint (VirtualNetworkRule) verili ad alanı için NetworkRuleSet 'e ekler</span><span class="sxs-lookup"><span data-stu-id="fc5da-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="fc5da-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fc5da-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="fc5da-114">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="fc5da-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="fc5da-115">Verilen ad alanı için $virtualruleset 1 öğesini NetworkRuleSet 'e ekler</span><span class="sxs-lookup"><span data-stu-id="fc5da-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="fc5da-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc5da-116">PARAMETERS</span></span>

### <span data-ttu-id="fc5da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5da-117">-DefaultProfile</span></span>
<span data-ttu-id="fc5da-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc5da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5da-119">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="fc5da-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="fc5da-120">Alt ağın ARM KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="fc5da-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5da-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc5da-121">-Name</span></span>
<span data-ttu-id="fc5da-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="fc5da-122">Namespace Name</span></span>

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

### <span data-ttu-id="fc5da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5da-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc5da-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fc5da-124">Resource Group Name</span></span>

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

### <span data-ttu-id="fc5da-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fc5da-125">-SubnetId</span></span>
<span data-ttu-id="fc5da-126">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="fc5da-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5da-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="fc5da-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="fc5da-128">VirtualNetworkRule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="fc5da-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5da-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc5da-129">-Confirm</span></span>
<span data-ttu-id="fc5da-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc5da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5da-131">-WhatIf</span></span>
<span data-ttu-id="fc5da-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc5da-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5da-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc5da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5da-134">CommonParameters</span></span>
<span data-ttu-id="fc5da-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc5da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fc5da-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5da-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5da-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc5da-137">INPUTS</span></span>

### <span data-ttu-id="fc5da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fc5da-138">System.String</span></span>

### <span data-ttu-id="fc5da-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc5da-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fc5da-140">Microsoft. Azure. Commands. ServiceBus. modeller. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="fc5da-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="fc5da-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc5da-141">OUTPUTS</span></span>

### <span data-ttu-id="fc5da-142">Microsoft. Azure. Commands. ServiceBus. modeller. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="fc5da-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="fc5da-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc5da-143">NOTES</span></span>

## <span data-ttu-id="fc5da-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc5da-144">RELATED LINKS</span></span>