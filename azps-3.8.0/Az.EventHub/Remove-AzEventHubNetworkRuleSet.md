---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937516"
---
# <span data-ttu-id="4db97-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4db97-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="4db97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db97-102">SYNOPSIS</span></span>
<span data-ttu-id="4db97-103">Verilen ad alanı için NetworkRuleSet 'i kaldırır</span><span class="sxs-lookup"><span data-stu-id="4db97-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="4db97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4db97-104">SYNTAX</span></span>

### <span data-ttu-id="4db97-105">NetworkRuleSetPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4db97-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db97-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4db97-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db97-107">Networkrulesetresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4db97-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db97-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4db97-108">DESCRIPTION</span></span>
<span data-ttu-id="4db97-109">Verilen ad alanı için NetworkRuleSet 'i kaldırır</span><span class="sxs-lookup"><span data-stu-id="4db97-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="4db97-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4db97-110">EXAMPLES</span></span>

### <span data-ttu-id="4db97-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4db97-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="4db97-112">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="4db97-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="4db97-113">Verilen "Eventhub-Namespace1-1375" ad alanı için NetworkRuleSet 'i siler</span><span class="sxs-lookup"><span data-stu-id="4db97-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="4db97-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4db97-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="4db97-115">InputObject kullanarak NetworkRuleSet 'i siler</span><span class="sxs-lookup"><span data-stu-id="4db97-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="4db97-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4db97-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="4db97-117">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="4db97-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="4db97-118">Ad alanının ResourceId kullanarak NetworkRuleSet 'i siler</span><span class="sxs-lookup"><span data-stu-id="4db97-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="4db97-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4db97-119">PARAMETERS</span></span>

### <span data-ttu-id="4db97-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="4db97-120">-AsJob</span></span>
<span data-ttu-id="4db97-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4db97-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4db97-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db97-122">-DefaultProfile</span></span>
<span data-ttu-id="4db97-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4db97-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db97-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4db97-124">-InputObject</span></span>
<span data-ttu-id="4db97-125">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="4db97-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4db97-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4db97-126">-Name</span></span>
<span data-ttu-id="4db97-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="4db97-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db97-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4db97-128">-PassThru</span></span>
<span data-ttu-id="4db97-129">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="4db97-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4db97-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db97-130">-ResourceGroupName</span></span>
<span data-ttu-id="4db97-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4db97-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db97-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4db97-132">-ResourceId</span></span>
<span data-ttu-id="4db97-133">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4db97-133">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db97-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="4db97-134">-Confirm</span></span>
<span data-ttu-id="4db97-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4db97-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db97-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db97-136">-WhatIf</span></span>
<span data-ttu-id="4db97-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4db97-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db97-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4db97-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db97-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db97-139">CommonParameters</span></span>
<span data-ttu-id="4db97-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4db97-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4db97-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db97-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db97-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4db97-142">INPUTS</span></span>

### <span data-ttu-id="4db97-143">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4db97-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="4db97-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4db97-144">System.String</span></span>

## <span data-ttu-id="4db97-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4db97-145">OUTPUTS</span></span>

### <span data-ttu-id="4db97-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4db97-146">System.Boolean</span></span>

## <span data-ttu-id="4db97-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4db97-147">NOTES</span></span>

## <span data-ttu-id="4db97-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4db97-148">RELATED LINKS</span></span>