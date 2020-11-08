---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277452"
---
# <span data-ttu-id="89f50-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="89f50-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="89f50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89f50-102">SYNOPSIS</span></span>
<span data-ttu-id="89f50-103">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="89f50-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="89f50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89f50-104">SYNTAX</span></span>

### <span data-ttu-id="89f50-105">Iprulepropertiesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89f50-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89f50-106">Ipruleinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="89f50-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89f50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89f50-107">DESCRIPTION</span></span>
<span data-ttu-id="89f50-108">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="89f50-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="89f50-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89f50-109">EXAMPLES</span></span>

### <span data-ttu-id="89f50-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89f50-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="89f50-111">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="89f50-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="89f50-112">verilen ad alanıyla ilgili olarak IPMask "11.22.33.44" ile birlikte</span><span class="sxs-lookup"><span data-stu-id="89f50-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="89f50-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="89f50-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="89f50-114">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="89f50-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="89f50-115">verilen ad alanıyla ilgili olarak IPMask "11.22.33.44" ile birlikte</span><span class="sxs-lookup"><span data-stu-id="89f50-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="89f50-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89f50-116">PARAMETERS</span></span>

### <span data-ttu-id="89f50-117">-Eylem</span><span class="sxs-lookup"><span data-stu-id="89f50-117">-Action</span></span>
<span data-ttu-id="89f50-118">IP filtre eylemi</span><span class="sxs-lookup"><span data-stu-id="89f50-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="89f50-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f50-119">-DefaultProfile</span></span>
<span data-ttu-id="89f50-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89f50-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f50-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="89f50-121">-IpMask</span></span>
<span data-ttu-id="89f50-122">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="89f50-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="89f50-123">-Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="89f50-123">-IpRuleObject</span></span>
<span data-ttu-id="89f50-124">Eklenecek ıprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="89f50-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="89f50-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="89f50-125">-Name</span></span>
<span data-ttu-id="89f50-126">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="89f50-126">Namespace Name</span></span>

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

### <span data-ttu-id="89f50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f50-127">-ResourceGroupName</span></span>
<span data-ttu-id="89f50-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="89f50-128">Resource Group Name</span></span>

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

### <span data-ttu-id="89f50-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="89f50-129">-Confirm</span></span>
<span data-ttu-id="89f50-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89f50-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f50-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f50-131">-WhatIf</span></span>
<span data-ttu-id="89f50-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89f50-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f50-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89f50-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f50-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f50-134">CommonParameters</span></span>
<span data-ttu-id="89f50-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89f50-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="89f50-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f50-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f50-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89f50-137">INPUTS</span></span>

### <span data-ttu-id="89f50-138">System. String</span><span class="sxs-lookup"><span data-stu-id="89f50-138">System.String</span></span>

### <span data-ttu-id="89f50-139">Microsoft. Azure. Commands. EventHub. model. Psnwrulesetıprulesattributes</span><span class="sxs-lookup"><span data-stu-id="89f50-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="89f50-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89f50-140">OUTPUTS</span></span>

### <span data-ttu-id="89f50-141">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="89f50-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="89f50-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89f50-142">NOTES</span></span>

## <span data-ttu-id="89f50-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89f50-143">RELATED LINKS</span></span>
