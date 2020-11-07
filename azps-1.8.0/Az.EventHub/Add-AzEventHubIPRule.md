---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 959fcab661139a1cacae46a315db0eaa93f0c09e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760859"
---
# <span data-ttu-id="1bd6d-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="1bd6d-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="1bd6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd6d-103">Verilen ad alanının NetworkRuleSet öğesine tek bir ıprule ekleme</span><span class="sxs-lookup"><span data-stu-id="1bd6d-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1bd6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1bd6d-104">SYNTAX</span></span>

### <span data-ttu-id="1bd6d-105">Iprulepropertiesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1bd6d-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd6d-106">Ipruleinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="1bd6d-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bd6d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bd6d-107">DESCRIPTION</span></span>
<span data-ttu-id="1bd6d-108">Verilen ad alanının NetworkRuleSet öğesine tek bir ıprule ekleme</span><span class="sxs-lookup"><span data-stu-id="1bd6d-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1bd6d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1bd6d-109">EXAMPLES</span></span>

### <span data-ttu-id="1bd6d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1bd6d-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="1bd6d-111">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="1bd6d-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="1bd6d-112">verilen Namesapce için IPMask "11.22.33.44" ile birlikte</span><span class="sxs-lookup"><span data-stu-id="1bd6d-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

### <span data-ttu-id="1bd6d-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1bd6d-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="1bd6d-114">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="1bd6d-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="1bd6d-115">verilen Namesapce için IPMask "11.22.33.44" ile birlikte</span><span class="sxs-lookup"><span data-stu-id="1bd6d-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

## <span data-ttu-id="1bd6d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1bd6d-116">PARAMETERS</span></span>

### <span data-ttu-id="1bd6d-117">-Eylem</span><span class="sxs-lookup"><span data-stu-id="1bd6d-117">-Action</span></span>
<span data-ttu-id="1bd6d-118">IP filtre eylemi</span><span class="sxs-lookup"><span data-stu-id="1bd6d-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="1bd6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd6d-119">-DefaultProfile</span></span>
<span data-ttu-id="1bd6d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1bd6d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bd6d-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="1bd6d-121">-IpMask</span></span>
<span data-ttu-id="1bd6d-122">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="1bd6d-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="1bd6d-123">-Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="1bd6d-123">-IpRuleObject</span></span>
<span data-ttu-id="1bd6d-124">Eklenecek ıprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="1bd6d-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd6d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1bd6d-125">-Name</span></span>
<span data-ttu-id="1bd6d-126">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="1bd6d-126">Namespace Name</span></span>

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

### <span data-ttu-id="1bd6d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd6d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bd6d-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1bd6d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1bd6d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="1bd6d-129">-Confirm</span></span>
<span data-ttu-id="1bd6d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1bd6d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bd6d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bd6d-131">-WhatIf</span></span>
<span data-ttu-id="1bd6d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1bd6d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bd6d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1bd6d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bd6d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd6d-134">CommonParameters</span></span>
<span data-ttu-id="1bd6d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1bd6d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1bd6d-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd6d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd6d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1bd6d-137">INPUTS</span></span>

### <span data-ttu-id="1bd6d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1bd6d-138">System.String</span></span>

### <span data-ttu-id="1bd6d-139">Microsoft. Azure. Commands. EventHub. model. Psnwrulesetıprulesattributes</span><span class="sxs-lookup"><span data-stu-id="1bd6d-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="1bd6d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1bd6d-140">OUTPUTS</span></span>

### <span data-ttu-id="1bd6d-141">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1bd6d-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1bd6d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1bd6d-142">NOTES</span></span>

## <span data-ttu-id="1bd6d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1bd6d-143">RELATED LINKS</span></span>
