---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275257"
---
# <span data-ttu-id="0a6c5-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0a6c5-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="0a6c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6c5-103">Güvenlik duvarı ilkesi için ManagedRules oluşturma.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="0a6c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a6c5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a6c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6c5-106">**Yeni-AzApplicationGatewayFirewallPolicyManagedRule** , güvenlik duvarı ilkesi için yönetilen kurallar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="0a6c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6c5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0a6c5-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="0a6c5-109">Bu komut, $managedRuleSet içeren bir ManagedRuleSet listesi ve girdileri $exclusion 1, $exclusion 2 olan bir dışlama listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="0a6c5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a6c5-110">PARAMETERS</span></span>

### <span data-ttu-id="0a6c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6c5-111">-DefaultProfile</span></span>
<span data-ttu-id="0a6c5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6c5-113">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="0a6c5-113">-Exclusion</span></span>
<span data-ttu-id="0a6c5-114">Dışlama girdisinin listesi.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6c5-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a6c5-115">-ManagedRuleSet</span></span>
<span data-ttu-id="0a6c5-116">Yönetilen ruleSets 'in listesi.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6c5-117">CommonParameters</span></span>
<span data-ttu-id="0a6c5-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6c5-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6c5-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a6c5-120">INPUTS</span></span>

### <span data-ttu-id="0a6c5-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0a6c5-121">None</span></span>

## <span data-ttu-id="0a6c5-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a6c5-122">OUTPUTS</span></span>

### <span data-ttu-id="0a6c5-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="0a6c5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="0a6c5-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a6c5-124">NOTES</span></span>

## <span data-ttu-id="0a6c5-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a6c5-125">RELATED LINKS</span></span>
