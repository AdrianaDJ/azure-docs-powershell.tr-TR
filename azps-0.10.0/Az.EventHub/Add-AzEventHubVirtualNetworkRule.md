---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 37f13534095341895a4fc3b4c1c9feb9e5e911be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935907"
---
# <span data-ttu-id="99c23-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="99c23-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="99c23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c23-102">SYNOPSIS</span></span>
<span data-ttu-id="99c23-103">Verilen ad alanı için NetworkRuleSet 'e tek VirtualNetworkRule ekleme</span><span class="sxs-lookup"><span data-stu-id="99c23-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="99c23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99c23-104">SYNTAX</span></span>

### <span data-ttu-id="99c23-105">VirtualNetworkRulePropertiesParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99c23-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99c23-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99c23-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99c23-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99c23-107">DESCRIPTION</span></span>
<span data-ttu-id="99c23-108">Verilen ad alanı için NetworkRuleSet 'e tek VirtualNetworkRule ekleme</span><span class="sxs-lookup"><span data-stu-id="99c23-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="99c23-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99c23-109">EXAMPLES</span></span>

### <span data-ttu-id="99c23-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99c23-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="99c23-111">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="99c23-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="99c23-112">Verilen alt ağ ve ıgnoremissingvnetserviceendpoint (VirtualNetworkRule) verili ad alanı için NetworkRuleSet 'e ekler</span><span class="sxs-lookup"><span data-stu-id="99c23-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="99c23-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="99c23-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="99c23-114">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="99c23-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="99c23-115">Verilen ad alanı için $virtualruleset 1 öğesini NetworkRuleSet 'e ekler</span><span class="sxs-lookup"><span data-stu-id="99c23-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="99c23-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99c23-116">PARAMETERS</span></span>

### <span data-ttu-id="99c23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c23-117">-DefaultProfile</span></span>
<span data-ttu-id="99c23-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99c23-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c23-119">-Ignoremissingvnetserviceendpoint</span><span class="sxs-lookup"><span data-stu-id="99c23-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="99c23-120">Alt ağın ARM KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="99c23-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="99c23-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="99c23-121">-Name</span></span>
<span data-ttu-id="99c23-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="99c23-122">Namespace Name</span></span>

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

### <span data-ttu-id="99c23-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c23-123">-ResourceGroupName</span></span>
<span data-ttu-id="99c23-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="99c23-124">Resource Group Name</span></span>

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

### <span data-ttu-id="99c23-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99c23-125">-SubnetId</span></span>
<span data-ttu-id="99c23-126">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="99c23-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="99c23-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="99c23-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="99c23-128">VirtualNetworkRule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="99c23-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99c23-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="99c23-129">-Confirm</span></span>
<span data-ttu-id="99c23-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99c23-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c23-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c23-131">-WhatIf</span></span>
<span data-ttu-id="99c23-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99c23-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c23-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99c23-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c23-134">CommonParameters</span></span>
<span data-ttu-id="99c23-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99c23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="99c23-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c23-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c23-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99c23-137">INPUTS</span></span>

### <span data-ttu-id="99c23-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99c23-138">System.String</span></span>

### <span data-ttu-id="99c23-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99c23-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="99c23-140">Microsoft. Azure. Commands. EventHub. model. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="99c23-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="99c23-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99c23-141">OUTPUTS</span></span>

### <span data-ttu-id="99c23-142">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="99c23-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="99c23-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99c23-143">NOTES</span></span>

## <span data-ttu-id="99c23-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99c23-144">RELATED LINKS</span></span>
