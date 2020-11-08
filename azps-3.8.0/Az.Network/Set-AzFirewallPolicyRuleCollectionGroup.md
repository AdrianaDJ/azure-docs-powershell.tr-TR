---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097987"
---
# <span data-ttu-id="2ad2b-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="2ad2b-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="2ad2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ad2b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad2b-103">değiştirilmiş bir Azure Güvenlik duvarı ilkesi kuralı koleksiyon grubunu kaydeder</span><span class="sxs-lookup"><span data-stu-id="2ad2b-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="2ad2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ad2b-104">SYNTAX</span></span>

### <span data-ttu-id="2ad2b-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ad2b-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad2b-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ad2b-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad2b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ad2b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad2b-108">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2ad2b-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad2b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ad2b-109">DESCRIPTION</span></span>
<span data-ttu-id="2ad2b-110">**Set-AzFirewallPolicyRuleCollectionGroup** cmdlet 'i, bir Azure Güvenlik duvarı ilkesinde bir kural koleksiyonu gruplarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="2ad2b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ad2b-111">EXAMPLES</span></span>

### <span data-ttu-id="2ad2b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ad2b-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="2ad2b-113">Bu örnekte, güvenlik duvarı ilkesinde bir kural koleksiyonu grubu güncelleştirilir $fp</span><span class="sxs-lookup"><span data-stu-id="2ad2b-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="2ad2b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ad2b-114">PARAMETERS</span></span>

### <span data-ttu-id="2ad2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad2b-115">-DefaultProfile</span></span>
<span data-ttu-id="2ad2b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad2b-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="2ad2b-117">-FirewallPolicyName</span></span>
<span data-ttu-id="2ad2b-118">Güvenlik Duvarı ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="2ad2b-118">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="2ad2b-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="2ad2b-120">Güvenlik Duvarı Ilkesi.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad2b-121">-InputObject</span></span>
<span data-ttu-id="2ad2b-122">Kural listesi</span><span class="sxs-lookup"><span data-stu-id="2ad2b-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ad2b-123">-Name</span></span>
<span data-ttu-id="2ad2b-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-125">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="2ad2b-125">-Priority</span></span>
<span data-ttu-id="2ad2b-126">Kural grubunun önceliği</span><span class="sxs-lookup"><span data-stu-id="2ad2b-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ad2b-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ad2b-129">-ResourceId</span></span>
<span data-ttu-id="2ad2b-130">Kural koleksiyonu grup kimliği</span><span class="sxs-lookup"><span data-stu-id="2ad2b-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="2ad2b-131">-RuleCollection</span></span>
<span data-ttu-id="2ad2b-132">Kural koleksiyonlarının listesi</span><span class="sxs-lookup"><span data-stu-id="2ad2b-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad2b-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ad2b-133">-Confirm</span></span>
<span data-ttu-id="2ad2b-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad2b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad2b-135">-WhatIf</span></span>
<span data-ttu-id="2ad2b-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad2b-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad2b-138">CommonParameters</span></span>
<span data-ttu-id="2ad2b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad2b-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ad2b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad2b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ad2b-141">INPUTS</span></span>

### <span data-ttu-id="2ad2b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2ad2b-142">System.String</span></span>

### <span data-ttu-id="2ad2b-143">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2ad2b-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="2ad2b-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ad2b-144">OUTPUTS</span></span>

### <span data-ttu-id="2ad2b-145">Microsoft. Azure. Commands. Network. model. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="2ad2b-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="2ad2b-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ad2b-146">NOTES</span></span>

## <span data-ttu-id="2ad2b-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ad2b-147">RELATED LINKS</span></span>
