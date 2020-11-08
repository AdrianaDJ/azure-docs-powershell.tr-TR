---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109480"
---
# <span data-ttu-id="24679-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="24679-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="24679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24679-102">SYNOPSIS</span></span>
<span data-ttu-id="24679-103">RuleGroupOverrideGroup girişi için bir managedRuleOverride girdisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24679-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="24679-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24679-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24679-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24679-105">DESCRIPTION</span></span>
<span data-ttu-id="24679-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** bir ruleoverride girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24679-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="24679-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24679-107">EXAMPLES</span></span>

### <span data-ttu-id="24679-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24679-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="24679-109">$RuleId olarak RuleId ve devre dışı durumu içeren bir ruleOverride girdisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24679-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="24679-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24679-110">PARAMETERS</span></span>

### <span data-ttu-id="24679-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24679-111">-DefaultProfile</span></span>
<span data-ttu-id="24679-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24679-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24679-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="24679-113">-RuleId</span></span>
<span data-ttu-id="24679-114">Kural girişinde RuleId belirtin.</span><span class="sxs-lookup"><span data-stu-id="24679-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="24679-115">Durumlu</span><span class="sxs-lookup"><span data-stu-id="24679-115">-State</span></span>
<span data-ttu-id="24679-116">Kural girişinde RuleId belirtin.</span><span class="sxs-lookup"><span data-stu-id="24679-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24679-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24679-117">CommonParameters</span></span>
<span data-ttu-id="24679-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24679-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24679-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="24679-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24679-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24679-120">INPUTS</span></span>

### <span data-ttu-id="24679-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="24679-121">None</span></span>

## <span data-ttu-id="24679-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24679-122">OUTPUTS</span></span>

### <span data-ttu-id="24679-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="24679-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="24679-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24679-124">NOTES</span></span>

## <span data-ttu-id="24679-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24679-125">RELATED LINKS</span></span>
