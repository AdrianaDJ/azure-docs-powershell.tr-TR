---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 146c6157163209fabb8472ef7602d223bb344530
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932451"
---
# <span data-ttu-id="f36fa-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f36fa-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="f36fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f36fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f36fa-103">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="f36fa-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="f36fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f36fa-104">SYNTAX</span></span>

### <span data-ttu-id="f36fa-105">VirtualNetworkRulePropertiesParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f36fa-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f36fa-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f36fa-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f36fa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f36fa-107">DESCRIPTION</span></span>
<span data-ttu-id="f36fa-108">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="f36fa-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="f36fa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f36fa-109">EXAMPLES</span></span>

### <span data-ttu-id="f36fa-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f36fa-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="f36fa-111">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="f36fa-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="f36fa-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f36fa-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="f36fa-113">Verilen ad alanı için NetworkRuleSet 'in $virtualruleset 1 öğesini kaldır</span><span class="sxs-lookup"><span data-stu-id="f36fa-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="f36fa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f36fa-114">PARAMETERS</span></span>

### <span data-ttu-id="f36fa-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="f36fa-115">-AsJob</span></span>
<span data-ttu-id="f36fa-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f36fa-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36fa-117">-DefaultProfile</span></span>
<span data-ttu-id="f36fa-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f36fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f36fa-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f36fa-119">-Name</span></span>
<span data-ttu-id="f36fa-120">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="f36fa-120">Namespace Name</span></span>

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

### <span data-ttu-id="f36fa-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f36fa-121">-PassThru</span></span>
<span data-ttu-id="f36fa-122">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f36fa-122">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="f36fa-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f36fa-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f36fa-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f36fa-125">-SubnetId</span></span>
<span data-ttu-id="f36fa-126">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="f36fa-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="f36fa-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f36fa-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="f36fa-128">Iprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="f36fa-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="f36fa-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="f36fa-129">-Confirm</span></span>
<span data-ttu-id="f36fa-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f36fa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f36fa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f36fa-131">-WhatIf</span></span>
<span data-ttu-id="f36fa-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f36fa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f36fa-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f36fa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f36fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36fa-134">CommonParameters</span></span>
<span data-ttu-id="f36fa-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f36fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f36fa-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f36fa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36fa-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f36fa-137">INPUTS</span></span>

### <span data-ttu-id="f36fa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f36fa-138">System.String</span></span>

### <span data-ttu-id="f36fa-139">Microsoft. Azure. Commands. ServiceBus. modeller. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f36fa-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="f36fa-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f36fa-140">OUTPUTS</span></span>

### <span data-ttu-id="f36fa-141">Microsoft. Azure. Commands. ServiceBus. modeller. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f36fa-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f36fa-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f36fa-142">NOTES</span></span>

## <span data-ttu-id="f36fa-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f36fa-143">RELATED LINKS</span></span>
