---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104812"
---
# <span data-ttu-id="c03df-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="c03df-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="c03df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c03df-102">SYNOPSIS</span></span>
<span data-ttu-id="c03df-103">FirewallPolicy için bir ManagedRuleSet oluşturur</span><span class="sxs-lookup"><span data-stu-id="c03df-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="c03df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c03df-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c03df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c03df-105">DESCRIPTION</span></span>
<span data-ttu-id="c03df-106">**Yeni-AzApplicationGatewayFirewallPolicyManagedRuleSet** , güvenlik duvarı ilkesi için yönetilen kurallar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c03df-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="c03df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c03df-107">EXAMPLES</span></span>

### <span data-ttu-id="c03df-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c03df-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="c03df-109">$RuleSetType olarak ruleSetType ile birlikte bir ManagedRuleSet oluşturur, $ruleSetVersion olarak ruleSetVersion, ve $managedRuleSet $ruleGroupOverride $ruleGroupOverride RuleGroupOverrides olarak</span><span class="sxs-lookup"><span data-stu-id="c03df-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="c03df-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c03df-110">PARAMETERS</span></span>

### <span data-ttu-id="c03df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c03df-111">-DefaultProfile</span></span>
<span data-ttu-id="c03df-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c03df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c03df-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c03df-113">-RuleGroupOverride</span></span>
<span data-ttu-id="c03df-114">Kural grubu geçersiz kılmaları.</span><span class="sxs-lookup"><span data-stu-id="c03df-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c03df-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="c03df-115">-RuleSetType</span></span>
<span data-ttu-id="c03df-116">ManagedRuleSet 'te RuleSetType belirtme</span><span class="sxs-lookup"><span data-stu-id="c03df-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="c03df-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="c03df-117">-RuleSetVersion</span></span>
<span data-ttu-id="c03df-118">ManagedRuleSet 'te RuleSetVersion belirtme</span><span class="sxs-lookup"><span data-stu-id="c03df-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="c03df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c03df-119">CommonParameters</span></span>
<span data-ttu-id="c03df-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c03df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c03df-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c03df-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c03df-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c03df-122">INPUTS</span></span>

### <span data-ttu-id="c03df-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c03df-123">None</span></span>

## <span data-ttu-id="c03df-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c03df-124">OUTPUTS</span></span>

### <span data-ttu-id="c03df-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="c03df-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="c03df-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c03df-126">NOTES</span></span>

## <span data-ttu-id="c03df-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c03df-127">RELATED LINKS</span></span>
