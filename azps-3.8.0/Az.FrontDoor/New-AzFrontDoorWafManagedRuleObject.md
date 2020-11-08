---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 6e56ff9b174ec13d0844a1ac860d34043f8b73cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103836"
---
# <span data-ttu-id="8e6b3-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8e6b3-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="8e6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6b3-103">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8e6b3-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="8e6b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e6b3-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e6b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="8e6b3-106">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8e6b3-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="8e6b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e6b3-107">EXAMPLES</span></span>

### <span data-ttu-id="8e6b3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8e6b3-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="8e6b3-109">ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8e6b3-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="8e6b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e6b3-110">PARAMETERS</span></span>

### <span data-ttu-id="8e6b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6b3-111">-DefaultProfile</span></span>
<span data-ttu-id="8e6b3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e6b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e6b3-113">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="8e6b3-113">-Exclusion</span></span>
<span data-ttu-id="8e6b3-114">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="8e6b3-114">Exclusion</span></span>

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

### <span data-ttu-id="8e6b3-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8e6b3-115">-RuleGroupOverride</span></span>
<span data-ttu-id="8e6b3-116">Azure yönetilen sağlayıcısı geçersiz kılma yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="8e6b3-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e6b3-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="8e6b3-117">-Type</span></span>
<span data-ttu-id="8e6b3-118">RuleSet 'in türü</span><span class="sxs-lookup"><span data-stu-id="8e6b3-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="8e6b3-119">-Version</span><span class="sxs-lookup"><span data-stu-id="8e6b3-119">-Version</span></span>
<span data-ttu-id="8e6b3-120">RuleSet 'in sürümü</span><span class="sxs-lookup"><span data-stu-id="8e6b3-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="8e6b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6b3-121">CommonParameters</span></span>
<span data-ttu-id="8e6b3-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e6b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6b3-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8e6b3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6b3-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e6b3-124">INPUTS</span></span>

### <span data-ttu-id="8e6b3-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8e6b3-125">None</span></span>

## <span data-ttu-id="8e6b3-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e6b3-126">OUTPUTS</span></span>

### <span data-ttu-id="8e6b3-127">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="8e6b3-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="8e6b3-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e6b3-128">NOTES</span></span>

## <span data-ttu-id="8e6b3-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e6b3-129">RELATED LINKS</span></span>

<span data-ttu-id="8e6b3-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="8e6b3-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
