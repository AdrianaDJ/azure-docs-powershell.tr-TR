---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: b6035e991b585ba296a9fdc591ccbdb44dd1b089
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916723"
---
# <span data-ttu-id="34c4f-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="34c4f-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="34c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="34c4f-103">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="34c4f-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="34c4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34c4f-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34c4f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="34c4f-106">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="34c4f-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="34c4f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="34c4f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34c4f-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="34c4f-109">ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="34c4f-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="34c4f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="34c4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c4f-111">-DefaultProfile</span></span>
<span data-ttu-id="34c4f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34c4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34c4f-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="34c4f-113">-RuleGroupOverride</span></span>
<span data-ttu-id="34c4f-114">Azure yönetilen sağlayıcısı geçersiz kılma yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="34c4f-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="34c4f-115">-Tür</span><span class="sxs-lookup"><span data-stu-id="34c4f-115">-Type</span></span>
<span data-ttu-id="34c4f-116">RuleSet 'in türü</span><span class="sxs-lookup"><span data-stu-id="34c4f-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="34c4f-117">-Version</span><span class="sxs-lookup"><span data-stu-id="34c4f-117">-Version</span></span>
<span data-ttu-id="34c4f-118">RuleSet 'in sürümü</span><span class="sxs-lookup"><span data-stu-id="34c4f-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="34c4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c4f-119">CommonParameters</span></span>
<span data-ttu-id="34c4f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34c4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c4f-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34c4f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c4f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34c4f-122">INPUTS</span></span>

### <span data-ttu-id="34c4f-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="34c4f-123">None</span></span>

## <span data-ttu-id="34c4f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34c4f-124">OUTPUTS</span></span>

### <span data-ttu-id="34c4f-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="34c4f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="34c4f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34c4f-126">NOTES</span></span>

## <span data-ttu-id="34c4f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34c4f-127">RELATED LINKS</span></span>

<span data-ttu-id="34c4f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="34c4f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
