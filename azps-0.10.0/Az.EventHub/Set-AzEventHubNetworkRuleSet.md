---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9d66a6824cf2c84ed0414681a4d89bf3de8f31dd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936724"
---
# <span data-ttu-id="a96e4-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a96e4-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="a96e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a96e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a96e4-103">Geçerli Azure aboneliğindeki verilen ad alanının NetworkruleSet öğesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="a96e4-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a96e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a96e4-104">SYNTAX</span></span>

### <span data-ttu-id="a96e4-105">NetworkRuleSetPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a96e4-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96e4-106">NET, Krulesetinputobjectset</span><span class="sxs-lookup"><span data-stu-id="a96e4-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a96e4-107">Networkrulesetresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a96e4-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a96e4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a96e4-108">DESCRIPTION</span></span>
<span data-ttu-id="a96e4-109">Geçerli Azure aboneliğindeki verilen ad alanının NetworkruleSet öğesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="a96e4-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a96e4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a96e4-110">EXAMPLES</span></span>

### <span data-ttu-id="a96e4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a96e4-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="a96e4-112">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="a96e4-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a96e4-113">-Iprule ve-VirtualNetworkRule parametrelerini kullanarak NetworkRuleSet 'i güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a96e4-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="a96e4-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a96e4-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="a96e4-115">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="a96e4-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a96e4-116">-InputObject kullanarak NetworkRuleSet 'i güncelleyin</span><span class="sxs-lookup"><span data-stu-id="a96e4-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="a96e4-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a96e4-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="a96e4-118">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="a96e4-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="a96e4-119">Diğer ad alanının-ResourceId kullanarak NetworkRuleSet 'i güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="a96e4-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="a96e4-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a96e4-120">PARAMETERS</span></span>

### <span data-ttu-id="a96e4-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="a96e4-121">-DefaultAction</span></span>
<span data-ttu-id="a96e4-122">NetworkRuleSet için varsayılan eylem</span><span class="sxs-lookup"><span data-stu-id="a96e4-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96e4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96e4-123">-DefaultProfile</span></span>
<span data-ttu-id="a96e4-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a96e4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a96e4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a96e4-125">-InputObject</span></span>
<span data-ttu-id="a96e4-126">NetworkruleSet yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="a96e4-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e4-127">-Iprule</span><span class="sxs-lookup"><span data-stu-id="a96e4-127">-IPRule</span></span>
<span data-ttu-id="a96e4-128">Ipruleset 'in listesi</span><span class="sxs-lookup"><span data-stu-id="a96e4-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96e4-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="a96e4-129">-Name</span></span>
<span data-ttu-id="a96e4-130">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a96e4-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96e4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96e4-131">-ResourceGroupName</span></span>
<span data-ttu-id="a96e4-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a96e4-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96e4-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a96e4-133">-ResourceId</span></span>
<span data-ttu-id="a96e4-134">Ad alanının kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="a96e4-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96e4-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a96e4-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="a96e4-136">VirtualNetworkRules listesi</span><span class="sxs-lookup"><span data-stu-id="a96e4-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96e4-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a96e4-137">-Confirm</span></span>
<span data-ttu-id="a96e4-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a96e4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96e4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96e4-139">-WhatIf</span></span>
<span data-ttu-id="a96e4-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a96e4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a96e4-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a96e4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96e4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96e4-142">CommonParameters</span></span>
<span data-ttu-id="a96e4-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a96e4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a96e4-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a96e4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96e4-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a96e4-145">INPUTS</span></span>

### <span data-ttu-id="a96e4-146">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a96e4-146">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="a96e4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a96e4-147">System.String</span></span>

## <span data-ttu-id="a96e4-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a96e4-148">OUTPUTS</span></span>

### <span data-ttu-id="a96e4-149">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a96e4-149">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a96e4-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a96e4-150">NOTES</span></span>

## <span data-ttu-id="a96e4-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a96e4-151">RELATED LINKS</span></span>