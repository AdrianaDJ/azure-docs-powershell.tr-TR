---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 68aa2d4d0d5ba29cdb2c8ddf86d49c6be1280c88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108286"
---
# <span data-ttu-id="b2c82-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b2c82-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="b2c82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c82-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c82-103">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="b2c82-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="b2c82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2c82-104">SYNTAX</span></span>

### <span data-ttu-id="b2c82-105">VirtualNetworkRulePropertiesParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2c82-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c82-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2c82-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c82-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2c82-107">DESCRIPTION</span></span>
<span data-ttu-id="b2c82-108">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="b2c82-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="b2c82-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2c82-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c82-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2c82-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="b2c82-111">Ad alanının NetworkRuleSet için verilen tek VirtualNetworkRule öğesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="b2c82-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="b2c82-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b2c82-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="b2c82-113">Verilen ad alanı için NetworkRuleSet 'in $virtualruleset 1 öğesini kaldır</span><span class="sxs-lookup"><span data-stu-id="b2c82-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="b2c82-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2c82-114">PARAMETERS</span></span>

### <span data-ttu-id="b2c82-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="b2c82-115">-AsJob</span></span>
<span data-ttu-id="b2c82-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b2c82-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2c82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c82-117">-DefaultProfile</span></span>
<span data-ttu-id="b2c82-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2c82-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2c82-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2c82-119">-Name</span></span>
<span data-ttu-id="b2c82-120">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b2c82-120">Namespace Name</span></span>

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

### <span data-ttu-id="b2c82-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b2c82-121">-PassThru</span></span>
<span data-ttu-id="b2c82-122">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="b2c82-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b2c82-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c82-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2c82-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b2c82-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b2c82-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b2c82-125">-SubnetId</span></span>
<span data-ttu-id="b2c82-126">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="b2c82-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="b2c82-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b2c82-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="b2c82-128">Iprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="b2c82-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="b2c82-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2c82-129">-Confirm</span></span>
<span data-ttu-id="b2c82-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2c82-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c82-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c82-131">-WhatIf</span></span>
<span data-ttu-id="b2c82-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2c82-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c82-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b2c82-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c82-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c82-134">CommonParameters</span></span>
<span data-ttu-id="b2c82-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2c82-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b2c82-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c82-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c82-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2c82-137">INPUTS</span></span>

### <span data-ttu-id="b2c82-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b2c82-138">System.String</span></span>

### <span data-ttu-id="b2c82-139">Microsoft. Azure. Commands. EventHub. model. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b2c82-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="b2c82-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2c82-140">OUTPUTS</span></span>

### <span data-ttu-id="b2c82-141">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b2c82-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b2c82-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2c82-142">NOTES</span></span>

## <span data-ttu-id="b2c82-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2c82-143">RELATED LINKS</span></span>