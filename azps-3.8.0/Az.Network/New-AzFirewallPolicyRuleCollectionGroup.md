---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097290"
---
# <span data-ttu-id="ba210-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ba210-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ba210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba210-102">SYNOPSIS</span></span>
<span data-ttu-id="ba210-103">Yeni Azure Güvenlik Duvarı Ilkesi kuralı koleksiyon grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ba210-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="ba210-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba210-104">SYNTAX</span></span>

### <span data-ttu-id="ba210-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba210-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba210-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba210-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba210-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba210-107">DESCRIPTION</span></span>
<span data-ttu-id="ba210-108">**New-AzFirewallPolicyRuleCollectionGroup** cmdlet 'ı bir Azure Güvenlik duvarı ilkesinde bir kural koleksiyonu grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba210-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="ba210-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba210-109">EXAMPLES</span></span>

### <span data-ttu-id="ba210-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba210-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="ba210-111">Bu örnek, güvenlik duvarı ilkesinde bir kural koleksiyonu grubu oluşturur $fp</span><span class="sxs-lookup"><span data-stu-id="ba210-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="ba210-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba210-112">PARAMETERS</span></span>

### <span data-ttu-id="ba210-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba210-113">-DefaultProfile</span></span>
<span data-ttu-id="ba210-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba210-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba210-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="ba210-115">-FirewallPolicyName</span></span>
<span data-ttu-id="ba210-116">Güvenlik Duvarı ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="ba210-116">The name of the firewall policy</span></span>

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

### <span data-ttu-id="ba210-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ba210-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="ba210-118">Güvenlik Duvarı Ilkesi.</span><span class="sxs-lookup"><span data-stu-id="ba210-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba210-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba210-119">-Name</span></span>
<span data-ttu-id="ba210-120">Kural grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ba210-120">The name of the Rule Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba210-121">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="ba210-121">-Priority</span></span>
<span data-ttu-id="ba210-122">Kural grubunun önceliği</span><span class="sxs-lookup"><span data-stu-id="ba210-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba210-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba210-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba210-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ba210-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba210-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="ba210-125">-RuleCollection</span></span>
<span data-ttu-id="ba210-126">Kural listesi</span><span class="sxs-lookup"><span data-stu-id="ba210-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba210-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba210-127">-Confirm</span></span>
<span data-ttu-id="ba210-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba210-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba210-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba210-129">-WhatIf</span></span>
<span data-ttu-id="ba210-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba210-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba210-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba210-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba210-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba210-132">CommonParameters</span></span>
<span data-ttu-id="ba210-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba210-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba210-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba210-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba210-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba210-135">INPUTS</span></span>

### <span data-ttu-id="ba210-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ba210-136">System.String</span></span>

### <span data-ttu-id="ba210-137">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ba210-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="ba210-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba210-138">OUTPUTS</span></span>

### <span data-ttu-id="ba210-139">Microsoft. Azure. Commands. Network. model. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ba210-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ba210-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba210-140">NOTES</span></span>

## <span data-ttu-id="ba210-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba210-141">RELATED LINKS</span></span>