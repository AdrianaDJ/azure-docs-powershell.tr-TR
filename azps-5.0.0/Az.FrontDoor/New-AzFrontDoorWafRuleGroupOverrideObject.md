---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275446"
---
# <span data-ttu-id="07583-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="07583-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="07583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07583-102">SYNOPSIS</span></span>
<span data-ttu-id="07583-103">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="07583-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="07583-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07583-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07583-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07583-105">DESCRIPTION</span></span>
<span data-ttu-id="07583-106">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="07583-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="07583-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07583-107">EXAMPLES</span></span>

### <span data-ttu-id="07583-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07583-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="07583-109">RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="07583-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="07583-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07583-110">PARAMETERS</span></span>

### <span data-ttu-id="07583-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07583-111">-DefaultProfile</span></span>
<span data-ttu-id="07583-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07583-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07583-113">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="07583-113">-Exclusion</span></span>
<span data-ttu-id="07583-114">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="07583-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07583-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="07583-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="07583-116">Kural geçersiz kılma listesi</span><span class="sxs-lookup"><span data-stu-id="07583-116">Rule override list</span></span>

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

### <span data-ttu-id="07583-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="07583-117">-RuleGroupName</span></span>
<span data-ttu-id="07583-118">Bu geçersiz kılmaların uygulandığı kural grubu adı</span><span class="sxs-lookup"><span data-stu-id="07583-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="07583-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07583-119">CommonParameters</span></span>
<span data-ttu-id="07583-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07583-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07583-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07583-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07583-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07583-122">INPUTS</span></span>

### <span data-ttu-id="07583-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="07583-123">None</span></span>

## <span data-ttu-id="07583-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07583-124">OUTPUTS</span></span>

### <span data-ttu-id="07583-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="07583-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="07583-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07583-126">NOTES</span></span>

## <span data-ttu-id="07583-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07583-127">RELATED LINKS</span></span>

[<span data-ttu-id="07583-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="07583-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
