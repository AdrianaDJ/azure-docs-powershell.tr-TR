---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 9465ad8d6f66b62da8b224ab635ca45fed1a8ca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933214"
---
# <span data-ttu-id="0886e-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0886e-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="0886e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0886e-102">SYNOPSIS</span></span>
<span data-ttu-id="0886e-103">Geçerli Azure aboneliğindeki verilen ad alanının NetworkruleSet öğesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="0886e-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="0886e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0886e-104">SYNTAX</span></span>

### <span data-ttu-id="0886e-105">NetworkRuleSetPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0886e-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0886e-106">NET, Krulesetinputobjectset</span><span class="sxs-lookup"><span data-stu-id="0886e-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0886e-107">Networkrulesetresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0886e-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0886e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0886e-108">DESCRIPTION</span></span>
<span data-ttu-id="0886e-109">Geçerli Azure aboneliğindeki verilen ad alanının net, Kruleset 'i güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="0886e-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="0886e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0886e-110">EXAMPLES</span></span>

### <span data-ttu-id="0886e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0886e-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="0886e-112">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="0886e-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="0886e-113">-Iprule ve-VirtualNetworkRule parametrelerini kullanarak NetworkRuleSet 'i güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0886e-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="0886e-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0886e-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="0886e-115">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="0886e-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="0886e-116">-InputObject kullanarak NetworkRuleSet 'i güncelleyin</span><span class="sxs-lookup"><span data-stu-id="0886e-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="0886e-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0886e-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="0886e-118">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet ıprules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, true}</span><span class="sxs-lookup"><span data-stu-id="0886e-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="0886e-119">Diğer ad alanının-ResourceId kullanarak NetworkRuleSet 'i güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="0886e-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="0886e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0886e-120">PARAMETERS</span></span>

### <span data-ttu-id="0886e-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="0886e-121">-DefaultAction</span></span>
<span data-ttu-id="0886e-122">NetworkRuleSet için varsayılan eylem</span><span class="sxs-lookup"><span data-stu-id="0886e-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="0886e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0886e-123">-DefaultProfile</span></span>
<span data-ttu-id="0886e-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0886e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0886e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0886e-125">-InputObject</span></span>
<span data-ttu-id="0886e-126">NetworkruleSet yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="0886e-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0886e-127">-Iprule</span><span class="sxs-lookup"><span data-stu-id="0886e-127">-IPRule</span></span>
<span data-ttu-id="0886e-128">Ipruleset 'in listesi</span><span class="sxs-lookup"><span data-stu-id="0886e-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0886e-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="0886e-129">-Name</span></span>
<span data-ttu-id="0886e-130">EventHub ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="0886e-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="0886e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0886e-131">-ResourceGroupName</span></span>
<span data-ttu-id="0886e-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0886e-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="0886e-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0886e-133">-ResourceId</span></span>
<span data-ttu-id="0886e-134">Ad alanının kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="0886e-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="0886e-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0886e-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="0886e-136">VirtualNetworkRules listesi</span><span class="sxs-lookup"><span data-stu-id="0886e-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0886e-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="0886e-137">-Confirm</span></span>
<span data-ttu-id="0886e-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0886e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0886e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0886e-139">-WhatIf</span></span>
<span data-ttu-id="0886e-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0886e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0886e-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0886e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0886e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0886e-142">CommonParameters</span></span>
<span data-ttu-id="0886e-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0886e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0886e-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0886e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0886e-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0886e-145">INPUTS</span></span>

### <span data-ttu-id="0886e-146">Microsoft. Azure. Commands. ServiceBus. modeller. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="0886e-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="0886e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0886e-147">System.String</span></span>

## <span data-ttu-id="0886e-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0886e-148">OUTPUTS</span></span>

### <span data-ttu-id="0886e-149">Microsoft. Azure. Commands. ServiceBus. modeller. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="0886e-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="0886e-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0886e-150">NOTES</span></span>

## <span data-ttu-id="0886e-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0886e-151">RELATED LINKS</span></span>