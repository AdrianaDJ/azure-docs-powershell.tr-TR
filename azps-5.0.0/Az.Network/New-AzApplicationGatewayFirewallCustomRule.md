---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279951"
---
# <span data-ttu-id="e5f3f-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="e5f3f-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="e5f3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f3f-103">Uygulama ağ geçidi güvenlik duvarı ilkesi için yeni bir özel kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="e5f3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5f3f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5f3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5f3f-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f3f-106">**Yeni-AzApplicationGatewayFirewallCustomRule** , güvenlik duvarı ilkesi için özel bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="e5f3f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5f3f-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f3f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5f3f-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="e5f3f-109">Bu komut örnek kuralı, öncelik 1 adıyla yeni bir özel kural oluşturur ve kural türü koşul değişkeninde tanımlanan Condition ile eşleşme kuralı olacak şekilde eşleşen kural olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="e5f3f-110">Yeni Match özel kuralı $customRule kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="e5f3f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5f3f-111">PARAMETERS</span></span>

### <span data-ttu-id="e5f3f-112">-Eylem</span><span class="sxs-lookup"><span data-stu-id="e5f3f-112">-Action</span></span>
<span data-ttu-id="e5f3f-113">Eylem türü.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f3f-114">-DefaultProfile</span></span>
<span data-ttu-id="e5f3f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f3f-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e5f3f-116">-MatchCondition</span></span>
<span data-ttu-id="e5f3f-117">Eşleşme koşulları listesi.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f3f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5f3f-118">-Name</span></span>
<span data-ttu-id="e5f3f-119">Kuralın adı.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="e5f3f-120">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="e5f3f-120">-Priority</span></span>
<span data-ttu-id="e5f3f-121">Kuralın önceliğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-121">Describes priority of the rule.</span></span>
<span data-ttu-id="e5f3f-122">Daha yüksek bir değer içeren kuralların öncesinde değeri düşük olan kurallar değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f3f-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e5f3f-123">-RuleType</span></span>
<span data-ttu-id="e5f3f-124">Kural türünü açıklar.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f3f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f3f-125">CommonParameters</span></span>
<span data-ttu-id="e5f3f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5f3f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f3f-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f3f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f3f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5f3f-128">INPUTS</span></span>

### <span data-ttu-id="e5f3f-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e5f3f-129">None</span></span>

## <span data-ttu-id="e5f3f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5f3f-130">OUTPUTS</span></span>

### <span data-ttu-id="e5f3f-131">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="e5f3f-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="e5f3f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5f3f-132">NOTES</span></span>

## <span data-ttu-id="e5f3f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5f3f-133">RELATED LINKS</span></span>
