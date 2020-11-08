---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108280"
---
# <span data-ttu-id="058aa-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="058aa-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="058aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="058aa-102">SYNOPSIS</span></span>
<span data-ttu-id="058aa-103">Geçerli Azure aboneliğindeki verilen ad alanının NetworkruleSet öğesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="058aa-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="058aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="058aa-104">SYNTAX</span></span>

### <span data-ttu-id="058aa-105">NetworkRuleSetPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="058aa-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058aa-106">NET, Krulesetinputobjectset</span><span class="sxs-lookup"><span data-stu-id="058aa-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="058aa-107">Networkrulesetresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="058aa-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="058aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="058aa-108">DESCRIPTION</span></span>
<span data-ttu-id="058aa-109">Geçerli Azure aboneliğindeki verilen ad alanının NetworkruleSet öğesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="058aa-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="058aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="058aa-110">EXAMPLES</span></span>

### <span data-ttu-id="058aa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="058aa-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="058aa-112">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="058aa-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="058aa-113">-Iprule ve-VirtualNetworkRule parametrelerini kullanarak NetworkRuleSet 'i güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="058aa-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="058aa-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="058aa-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="058aa-115">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="058aa-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="058aa-116">-InputObject kullanarak NetworkRuleSet 'i güncelleyin</span><span class="sxs-lookup"><span data-stu-id="058aa-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="058aa-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="058aa-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="058aa-118">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="058aa-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="058aa-119">Diğer ad alanının-ResourceId kullanarak NetworkRuleSet 'i güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="058aa-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="058aa-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="058aa-120">PARAMETERS</span></span>

### <span data-ttu-id="058aa-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="058aa-121">-DefaultAction</span></span>
<span data-ttu-id="058aa-122">NetworkRuleSet için varsayılan eylem</span><span class="sxs-lookup"><span data-stu-id="058aa-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="058aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058aa-123">-DefaultProfile</span></span>
<span data-ttu-id="058aa-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="058aa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058aa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="058aa-125">-InputObject</span></span>
<span data-ttu-id="058aa-126">NetworkruleSet yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="058aa-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="058aa-127">-Iprule</span><span class="sxs-lookup"><span data-stu-id="058aa-127">-IPRule</span></span>
<span data-ttu-id="058aa-128">Ipruleset 'in listesi</span><span class="sxs-lookup"><span data-stu-id="058aa-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="058aa-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="058aa-129">-Name</span></span>
<span data-ttu-id="058aa-130">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="058aa-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="058aa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058aa-131">-ResourceGroupName</span></span>
<span data-ttu-id="058aa-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="058aa-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="058aa-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="058aa-133">-ResourceId</span></span>
<span data-ttu-id="058aa-134">Ad alanının kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="058aa-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="058aa-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="058aa-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="058aa-136">TrustedServiceAccessEnabled 'in etkinleştirilip etkinleştirilmediğini gösterir</span><span class="sxs-lookup"><span data-stu-id="058aa-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058aa-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="058aa-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="058aa-138">VirtualNetworkRules listesi</span><span class="sxs-lookup"><span data-stu-id="058aa-138">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="058aa-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="058aa-139">-Confirm</span></span>
<span data-ttu-id="058aa-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="058aa-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="058aa-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="058aa-141">-WhatIf</span></span>
<span data-ttu-id="058aa-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="058aa-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="058aa-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="058aa-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="058aa-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058aa-144">CommonParameters</span></span>
<span data-ttu-id="058aa-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="058aa-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="058aa-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="058aa-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058aa-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="058aa-147">INPUTS</span></span>

### <span data-ttu-id="058aa-148">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="058aa-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="058aa-149">System. String</span><span class="sxs-lookup"><span data-stu-id="058aa-149">System.String</span></span>

## <span data-ttu-id="058aa-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="058aa-150">OUTPUTS</span></span>

### <span data-ttu-id="058aa-151">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="058aa-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="058aa-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="058aa-152">NOTES</span></span>

## <span data-ttu-id="058aa-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="058aa-153">RELATED LINKS</span></span>