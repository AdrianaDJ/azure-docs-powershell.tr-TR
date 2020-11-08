---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 60074271c37097e266e0c8e2ca1e4ee2a35e577d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935909"
---
# <span data-ttu-id="58385-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="58385-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="58385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58385-102">SYNOPSIS</span></span>
<span data-ttu-id="58385-103">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="58385-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="58385-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58385-104">SYNTAX</span></span>

### <span data-ttu-id="58385-105">Iprulepropertiesparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58385-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58385-106">Ipruleinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="58385-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58385-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="58385-107">DESCRIPTION</span></span>
<span data-ttu-id="58385-108">Verilen ad alanının NetworkRuleSet öğesine tek bir IP kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="58385-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="58385-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58385-109">EXAMPLES</span></span>

### <span data-ttu-id="58385-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="58385-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="58385-111">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="58385-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="58385-112">verilen ad alanıyla ilgili olarak IPMask "11.22.33.44" ile birlikte</span><span class="sxs-lookup"><span data-stu-id="58385-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="58385-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="58385-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="58385-114">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default türü: Microsoft. Eventhub/namespaces/NetworkRuleSet ıprules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="58385-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="58385-115">verilen ad alanıyla ilgili olarak IPMask "11.22.33.44" ile birlikte</span><span class="sxs-lookup"><span data-stu-id="58385-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="58385-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58385-116">PARAMETERS</span></span>

### <span data-ttu-id="58385-117">-Eylem</span><span class="sxs-lookup"><span data-stu-id="58385-117">-Action</span></span>
<span data-ttu-id="58385-118">IP filtre eylemi</span><span class="sxs-lookup"><span data-stu-id="58385-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="58385-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58385-119">-DefaultProfile</span></span>
<span data-ttu-id="58385-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58385-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58385-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="58385-121">-IpMask</span></span>
<span data-ttu-id="58385-122">Alt ağ kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="58385-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="58385-123">-Ipruleobject</span><span class="sxs-lookup"><span data-stu-id="58385-123">-IpRuleObject</span></span>
<span data-ttu-id="58385-124">Eklenecek ıprule yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="58385-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="58385-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="58385-125">-Name</span></span>
<span data-ttu-id="58385-126">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="58385-126">Namespace Name</span></span>

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

### <span data-ttu-id="58385-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58385-127">-ResourceGroupName</span></span>
<span data-ttu-id="58385-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="58385-128">Resource Group Name</span></span>

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

### <span data-ttu-id="58385-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="58385-129">-Confirm</span></span>
<span data-ttu-id="58385-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58385-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58385-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58385-131">-WhatIf</span></span>
<span data-ttu-id="58385-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58385-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58385-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58385-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58385-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58385-134">CommonParameters</span></span>
<span data-ttu-id="58385-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58385-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="58385-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58385-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58385-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58385-137">INPUTS</span></span>

### <span data-ttu-id="58385-138">System. String</span><span class="sxs-lookup"><span data-stu-id="58385-138">System.String</span></span>

### <span data-ttu-id="58385-139">Microsoft. Azure. Commands. EventHub. model. Psnwrulesetıprulesattributes</span><span class="sxs-lookup"><span data-stu-id="58385-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="58385-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58385-140">OUTPUTS</span></span>

### <span data-ttu-id="58385-141">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="58385-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="58385-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58385-142">NOTES</span></span>

## <span data-ttu-id="58385-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58385-143">RELATED LINKS</span></span>