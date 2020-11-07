---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: bde2d2edd48edf83efaf7f548daf4f97d6cffbaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751889"
---
# <span data-ttu-id="6a6b5-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6a6b5-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="6a6b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6b5-103">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6b5-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6a6b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a6b5-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a6b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a6b5-105">DESCRIPTION</span></span>
<span data-ttu-id="6a6b5-106">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6b5-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6a6b5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a6b5-107">EXAMPLES</span></span>

### <span data-ttu-id="6a6b5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a6b5-108">Example 1</span></span>
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

<span data-ttu-id="6a6b5-109">ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6b5-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="6a6b5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a6b5-110">PARAMETERS</span></span>

### <span data-ttu-id="6a6b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6b5-111">-DefaultProfile</span></span>
<span data-ttu-id="6a6b5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a6b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a6b5-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6a6b5-113">-RuleGroupOverride</span></span>
<span data-ttu-id="6a6b5-114">Azure yönetilen sağlayıcısı geçersiz kılma yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="6a6b5-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="6a6b5-115">-Tür</span><span class="sxs-lookup"><span data-stu-id="6a6b5-115">-Type</span></span>
<span data-ttu-id="6a6b5-116">RuleSet 'in türü</span><span class="sxs-lookup"><span data-stu-id="6a6b5-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="6a6b5-117">-Version</span><span class="sxs-lookup"><span data-stu-id="6a6b5-117">-Version</span></span>
<span data-ttu-id="6a6b5-118">RuleSet 'in sürümü</span><span class="sxs-lookup"><span data-stu-id="6a6b5-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="6a6b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6b5-119">CommonParameters</span></span>
<span data-ttu-id="6a6b5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a6b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6b5-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6a6b5-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6b5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a6b5-122">INPUTS</span></span>

### <span data-ttu-id="6a6b5-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6a6b5-123">None</span></span>

## <span data-ttu-id="6a6b5-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a6b5-124">OUTPUTS</span></span>

### <span data-ttu-id="6a6b5-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="6a6b5-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="6a6b5-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a6b5-126">NOTES</span></span>

## <span data-ttu-id="6a6b5-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a6b5-127">RELATED LINKS</span></span>

<span data-ttu-id="6a6b5-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="6a6b5-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
