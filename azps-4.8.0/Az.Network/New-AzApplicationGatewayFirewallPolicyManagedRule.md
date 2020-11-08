---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274392"
---
# <span data-ttu-id="cbcd9-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="cbcd9-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="cbcd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbcd9-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcd9-103">Güvenlik duvarı ilkesi için ManagedRules oluşturma.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="cbcd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbcd9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbcd9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbcd9-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcd9-106">**Yeni-AzApplicationGatewayFirewallPolicyManagedRule** , güvenlik duvarı ilkesi için yönetilen kurallar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="cbcd9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbcd9-107">EXAMPLES</span></span>

### <span data-ttu-id="cbcd9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cbcd9-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="cbcd9-109">Bu komut, $managedRuleSet içeren bir ManagedRuleSet listesi ve girdileri $exclusion 1, $exclusion 2 olan bir dışlama listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="cbcd9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbcd9-110">PARAMETERS</span></span>

### <span data-ttu-id="cbcd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcd9-111">-DefaultProfile</span></span>
<span data-ttu-id="cbcd9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbcd9-113">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="cbcd9-113">-Exclusion</span></span>
<span data-ttu-id="cbcd9-114">Dışlama girdisinin listesi.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="cbcd9-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="cbcd9-115">-ManagedRuleSet</span></span>
<span data-ttu-id="cbcd9-116">Yönetilen ruleSets 'in listesi.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="cbcd9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcd9-117">CommonParameters</span></span>
<span data-ttu-id="cbcd9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcd9-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cbcd9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcd9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbcd9-120">INPUTS</span></span>

### <span data-ttu-id="cbcd9-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cbcd9-121">None</span></span>

## <span data-ttu-id="cbcd9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbcd9-122">OUTPUTS</span></span>

### <span data-ttu-id="cbcd9-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="cbcd9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="cbcd9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbcd9-124">NOTES</span></span>

## <span data-ttu-id="cbcd9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbcd9-125">RELATED LINKS</span></span>
