---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 8bfab06686cdabcb801b51b11298bf717f748770
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751887"
---
# <span data-ttu-id="90a1f-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="90a1f-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="90a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="90a1f-103">Yönetilen kural geçersiz kılma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="90a1f-103">Create managed rule override object</span></span>

## <span data-ttu-id="90a1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90a1f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90a1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="90a1f-106">Yönetilen WAF kural grubu için PSAzureManagedRuleOverride nesnesi oluşturma nesne oluşturma.</span><span class="sxs-lookup"><span data-stu-id="90a1f-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="90a1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90a1f-107">EXAMPLES</span></span>

### <span data-ttu-id="90a1f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90a1f-108">Example 1</span></span>
<span data-ttu-id="90a1f-109">942250 kuralı için yönetilen kural geçersiz kılma nesnesi oluşturun (SQLı grubunda).</span><span class="sxs-lookup"><span data-stu-id="90a1f-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="90a1f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90a1f-110">PARAMETERS</span></span>

### <span data-ttu-id="90a1f-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="90a1f-111">-Action</span></span>
<span data-ttu-id="90a1f-112">Geçersiz kılma eylemi</span><span class="sxs-lookup"><span data-stu-id="90a1f-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a1f-113">-DefaultProfile</span></span>
<span data-ttu-id="90a1f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90a1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90a1f-115">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="90a1f-115">-Disabled</span></span>
<span data-ttu-id="90a1f-116">Devre dışı durumu</span><span class="sxs-lookup"><span data-stu-id="90a1f-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a1f-117">-RuleId</span><span class="sxs-lookup"><span data-stu-id="90a1f-117">-RuleId</span></span>
<span data-ttu-id="90a1f-118">Kural KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="90a1f-118">Rule ID</span></span>

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

### <span data-ttu-id="90a1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a1f-119">CommonParameters</span></span>
<span data-ttu-id="90a1f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90a1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a1f-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90a1f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a1f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90a1f-122">INPUTS</span></span>

### <span data-ttu-id="90a1f-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="90a1f-123">None</span></span>

## <span data-ttu-id="90a1f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90a1f-124">OUTPUTS</span></span>

### <span data-ttu-id="90a1f-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="90a1f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="90a1f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90a1f-126">NOTES</span></span>

## <span data-ttu-id="90a1f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90a1f-127">RELATED LINKS</span></span>

[<span data-ttu-id="90a1f-128">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="90a1f-128">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)