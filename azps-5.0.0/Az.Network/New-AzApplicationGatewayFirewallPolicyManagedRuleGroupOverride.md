---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276199"
---
# <span data-ttu-id="7447b-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7447b-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="7447b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7447b-102">SYNOPSIS</span></span>
<span data-ttu-id="7447b-103">Güvenlik Duvarı ilkesinin ManagedRuleSets 'de RuleGroupOverride girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7447b-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="7447b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7447b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7447b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7447b-105">DESCRIPTION</span></span>
<span data-ttu-id="7447b-106">**Yeni-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** , bir güvenlik duvarı ilkesi Için bir managedrulepoverride girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7447b-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="7447b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7447b-107">EXAMPLES</span></span>

### <span data-ttu-id="7447b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7447b-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="7447b-109">$RuleName ve $rule 1 olarak, $rule 2 ' ye sahip grup adıyla bir RuleGroupOverride girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7447b-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="7447b-110">$overrideEntry aynı şekilde atanır</span><span class="sxs-lookup"><span data-stu-id="7447b-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="7447b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7447b-111">PARAMETERS</span></span>

### <span data-ttu-id="7447b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7447b-112">-DefaultProfile</span></span>
<span data-ttu-id="7447b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7447b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7447b-114">-Kural</span><span class="sxs-lookup"><span data-stu-id="7447b-114">-Rule</span></span>
<span data-ttu-id="7447b-115">Kural listesi.</span><span class="sxs-lookup"><span data-stu-id="7447b-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7447b-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="7447b-116">-RuleGroupName</span></span>
<span data-ttu-id="7447b-117">Geçersiz kılma kuralı grup girişinde ruleGroupName 'i belirtin.</span><span class="sxs-lookup"><span data-stu-id="7447b-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="7447b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7447b-118">CommonParameters</span></span>
<span data-ttu-id="7447b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7447b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7447b-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7447b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7447b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7447b-121">INPUTS</span></span>

### <span data-ttu-id="7447b-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7447b-122">None</span></span>

## <span data-ttu-id="7447b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7447b-123">OUTPUTS</span></span>

### <span data-ttu-id="7447b-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7447b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="7447b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7447b-125">NOTES</span></span>

## <span data-ttu-id="7447b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7447b-126">RELATED LINKS</span></span>
