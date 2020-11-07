---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 9385d8ca958eab28f485e56fbcd6c926f5422ca0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935863"
---
# <span data-ttu-id="6ceb4-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6ceb4-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="6ceb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ceb4-102">SYNOPSIS</span></span>
<span data-ttu-id="6ceb4-103">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6ceb4-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="6ceb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ceb4-104">SYNTAX</span></span>

### <span data-ttu-id="6ceb4-105">VirtualNetworkRulePropertiesParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ceb4-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ceb4-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ceb4-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ceb4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ceb4-107">DESCRIPTION</span></span>
<span data-ttu-id="6ceb4-108">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6ceb4-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="6ceb4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ceb4-109">EXAMPLES</span></span>

### <span data-ttu-id="6ceb4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ceb4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="6ceb4-111">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6ceb4-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="6ceb4-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6ceb4-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="6ceb4-113">Verilen ad alanı için NetworkRuleSet 'in $virtualruleset 1 öğesini kaldır</span><span class="sxs-lookup"><span data-stu-id="6ceb4-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="6ceb4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ceb4-114">PARAMETERS</span></span>

### <span data-ttu-id="6ceb4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="6ceb4-115">-AsJob</span></span>
<span data-ttu-id="6ceb4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6ceb4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ceb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ceb4-117">-DefaultProfile</span></span>
<span data-ttu-id="6ceb4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ceb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ceb4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ceb4-119">-Name</span></span>
<span data-ttu-id="6ceb4-120">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="6ceb4-120">Namespace Name</span></span>

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

### <span data-ttu-id="6ceb4-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6ceb4-121">-PassThru</span></span>
<span data-ttu-id="6ceb4-122">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6ceb4-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6ceb4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ceb4-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ceb4-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6ceb4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6ceb4-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6ceb4-125">-SubnetId</span></span>
<span data-ttu-id="6ceb4-126">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="6ceb4-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="6ceb4-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="6ceb4-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="6ceb4-128">Iprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="6ceb4-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="6ceb4-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ceb4-129">-Confirm</span></span>
<span data-ttu-id="6ceb4-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ceb4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ceb4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ceb4-131">-WhatIf</span></span>
<span data-ttu-id="6ceb4-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ceb4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ceb4-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ceb4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ceb4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ceb4-134">CommonParameters</span></span>
<span data-ttu-id="6ceb4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ceb4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6ceb4-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ceb4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ceb4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ceb4-137">INPUTS</span></span>

### <span data-ttu-id="6ceb4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6ceb4-138">System.String</span></span>

### <span data-ttu-id="6ceb4-139">Microsoft. Azure. Commands. EventHub. model. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6ceb4-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="6ceb4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ceb4-140">OUTPUTS</span></span>

### <span data-ttu-id="6ceb4-141">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="6ceb4-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="6ceb4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ceb4-142">NOTES</span></span>

## <span data-ttu-id="6ceb4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ceb4-143">RELATED LINKS</span></span>