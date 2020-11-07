---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 6175b99f5da139344c351189db5fbc5a13a137c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916712"
---
# <span data-ttu-id="15ff1-101">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="15ff1-101">New-AzFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="15ff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="15ff1-103">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="15ff1-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="15ff1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15ff1-104">SYNTAX</span></span>

```
New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15ff1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15ff1-105">DESCRIPTION</span></span>
<span data-ttu-id="15ff1-106">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="15ff1-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="15ff1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15ff1-107">EXAMPLES</span></span>

### <span data-ttu-id="15ff1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15ff1-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="15ff1-109">RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="15ff1-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="15ff1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15ff1-110">PARAMETERS</span></span>

### <span data-ttu-id="15ff1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ff1-111">-DefaultProfile</span></span>
<span data-ttu-id="15ff1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15ff1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15ff1-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="15ff1-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="15ff1-114">Kural geçersiz kılma listesi</span><span class="sxs-lookup"><span data-stu-id="15ff1-114">Rule override list</span></span>

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

### <span data-ttu-id="15ff1-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="15ff1-115">-RuleGroupName</span></span>
<span data-ttu-id="15ff1-116">Bu geçersiz kılmaların uygulandığı kural grubu adı</span><span class="sxs-lookup"><span data-stu-id="15ff1-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="15ff1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ff1-117">CommonParameters</span></span>
<span data-ttu-id="15ff1-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15ff1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ff1-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15ff1-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ff1-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15ff1-120">INPUTS</span></span>

### <span data-ttu-id="15ff1-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="15ff1-121">None</span></span>

## <span data-ttu-id="15ff1-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15ff1-122">OUTPUTS</span></span>

### <span data-ttu-id="15ff1-123">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="15ff1-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="15ff1-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15ff1-124">NOTES</span></span>

## <span data-ttu-id="15ff1-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15ff1-125">RELATED LINKS</span></span>

[<span data-ttu-id="15ff1-126">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="15ff1-126">New-AzFrontDoorManagedRuleObject</span></span>](./New-AzFrontDoorManagedRuleObject.md)
