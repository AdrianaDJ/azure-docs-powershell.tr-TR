---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107613"
---
# <span data-ttu-id="54e36-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="54e36-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="54e36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54e36-102">SYNOPSIS</span></span>
<span data-ttu-id="54e36-103">Verilen ad alanı için NetworkRuleSet 'i kaldırır</span><span class="sxs-lookup"><span data-stu-id="54e36-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="54e36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54e36-104">SYNTAX</span></span>

### <span data-ttu-id="54e36-105">NetworkRuleSetPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54e36-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e36-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54e36-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e36-107">Networkrulesetresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="54e36-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e36-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="54e36-108">DESCRIPTION</span></span>
<span data-ttu-id="54e36-109">Verilen ad alanı için NetworkRuleSet 'i kaldırır</span><span class="sxs-lookup"><span data-stu-id="54e36-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="54e36-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54e36-110">EXAMPLES</span></span>

### <span data-ttu-id="54e36-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="54e36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="54e36-112">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default türü: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="54e36-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="54e36-113">Verilen "ServiceBus-Namespace1-1375" ad alanı için NetworkRuleSet 'i siler</span><span class="sxs-lookup"><span data-stu-id="54e36-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="54e36-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="54e36-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="54e36-115">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="54e36-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="54e36-116">InputObject kullanarak NetworkRuleSet 'i siler</span><span class="sxs-lookup"><span data-stu-id="54e36-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="54e36-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="54e36-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="54e36-118">Ad: varsayılan DefaultAction: Izin verilen kimlik:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default türü: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="54e36-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="54e36-119">Ad alanının ResourceId kullanarak NetworkRuleSet 'i siler</span><span class="sxs-lookup"><span data-stu-id="54e36-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="54e36-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54e36-120">PARAMETERS</span></span>

### <span data-ttu-id="54e36-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="54e36-121">-AsJob</span></span>
<span data-ttu-id="54e36-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="54e36-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54e36-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e36-123">-DefaultProfile</span></span>
<span data-ttu-id="54e36-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54e36-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54e36-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54e36-125">-InputObject</span></span>
<span data-ttu-id="54e36-126">Namespace nesnesi</span><span class="sxs-lookup"><span data-stu-id="54e36-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54e36-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="54e36-127">-Name</span></span>
<span data-ttu-id="54e36-128">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="54e36-128">Namespace Name</span></span>

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

### <span data-ttu-id="54e36-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="54e36-129">-PassThru</span></span>
<span data-ttu-id="54e36-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="54e36-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="54e36-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e36-131">-ResourceGroupName</span></span>
<span data-ttu-id="54e36-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="54e36-132">Resource Group Name</span></span>

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

### <span data-ttu-id="54e36-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="54e36-133">-ResourceId</span></span>
<span data-ttu-id="54e36-134">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="54e36-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="54e36-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="54e36-135">-Confirm</span></span>
<span data-ttu-id="54e36-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54e36-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e36-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e36-137">-WhatIf</span></span>
<span data-ttu-id="54e36-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54e36-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e36-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54e36-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e36-140">CommonParameters</span></span>
<span data-ttu-id="54e36-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54e36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="54e36-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e36-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e36-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54e36-143">INPUTS</span></span>

### <span data-ttu-id="54e36-144">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="54e36-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="54e36-145">System. String</span><span class="sxs-lookup"><span data-stu-id="54e36-145">System.String</span></span>

## <span data-ttu-id="54e36-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54e36-146">OUTPUTS</span></span>

### <span data-ttu-id="54e36-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54e36-147">System.Boolean</span></span>

## <span data-ttu-id="54e36-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54e36-148">NOTES</span></span>

## <span data-ttu-id="54e36-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54e36-149">RELATED LINKS</span></span>
