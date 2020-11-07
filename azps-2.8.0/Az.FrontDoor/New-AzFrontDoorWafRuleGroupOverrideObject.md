---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: c55be8e72e3c5bb5418d3be4b74555eb20168113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751883"
---
# <span data-ttu-id="c001c-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="c001c-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="c001c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c001c-102">SYNOPSIS</span></span>
<span data-ttu-id="c001c-103">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c001c-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="c001c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c001c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c001c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c001c-105">DESCRIPTION</span></span>
<span data-ttu-id="c001c-106">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c001c-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="c001c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c001c-107">EXAMPLES</span></span>

### <span data-ttu-id="c001c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c001c-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="c001c-109">RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c001c-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="c001c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c001c-110">PARAMETERS</span></span>

### <span data-ttu-id="c001c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c001c-111">-DefaultProfile</span></span>
<span data-ttu-id="c001c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c001c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c001c-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="c001c-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="c001c-114">Kural geçersiz kılma listesi</span><span class="sxs-lookup"><span data-stu-id="c001c-114">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c001c-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="c001c-115">-RuleGroupName</span></span>
<span data-ttu-id="c001c-116">Bu geçersiz kılmaların uygulandığı kural grubu adı</span><span class="sxs-lookup"><span data-stu-id="c001c-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="c001c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c001c-117">CommonParameters</span></span>
<span data-ttu-id="c001c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c001c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c001c-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c001c-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c001c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c001c-120">INPUTS</span></span>

### <span data-ttu-id="c001c-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c001c-121">None</span></span>

## <span data-ttu-id="c001c-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c001c-122">OUTPUTS</span></span>

### <span data-ttu-id="c001c-123">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c001c-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="c001c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c001c-124">NOTES</span></span>

## <span data-ttu-id="c001c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c001c-125">RELATED LINKS</span></span>

[<span data-ttu-id="c001c-126">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c001c-126">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
