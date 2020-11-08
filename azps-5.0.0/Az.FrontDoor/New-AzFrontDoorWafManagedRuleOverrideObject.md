---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277397"
---
# <span data-ttu-id="90754-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="90754-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="90754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90754-102">SYNOPSIS</span></span>
<span data-ttu-id="90754-103">Yönetilen kural geçersiz kılma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="90754-103">Create managed rule override object</span></span>

## <span data-ttu-id="90754-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90754-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90754-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90754-105">DESCRIPTION</span></span>
<span data-ttu-id="90754-106">Yönetilen WAF kural grubu için PSAzureManagedRuleOverride nesnesi oluşturma nesne oluşturma.</span><span class="sxs-lookup"><span data-stu-id="90754-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="90754-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90754-107">EXAMPLES</span></span>

### <span data-ttu-id="90754-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90754-108">Example 1</span></span>
<span data-ttu-id="90754-109">942250 kuralı için yönetilen kural geçersiz kılma nesnesi oluşturun (SQLı grubunda).</span><span class="sxs-lookup"><span data-stu-id="90754-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="90754-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90754-110">PARAMETERS</span></span>

### <span data-ttu-id="90754-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="90754-111">-Action</span></span>
<span data-ttu-id="90754-112">Geçersiz kılma eylemi</span><span class="sxs-lookup"><span data-stu-id="90754-112">Override Action</span></span>

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

### <span data-ttu-id="90754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90754-113">-DefaultProfile</span></span>
<span data-ttu-id="90754-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90754-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90754-115">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="90754-115">-Disabled</span></span>
<span data-ttu-id="90754-116">Devre dışı durumu</span><span class="sxs-lookup"><span data-stu-id="90754-116">Disabled state</span></span>

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

### <span data-ttu-id="90754-117">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="90754-117">-Exclusion</span></span>
<span data-ttu-id="90754-118">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="90754-118">Exclusion</span></span>

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

### <span data-ttu-id="90754-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="90754-119">-RuleId</span></span>
<span data-ttu-id="90754-120">Kural KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="90754-120">Rule ID</span></span>

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

### <span data-ttu-id="90754-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90754-121">CommonParameters</span></span>
<span data-ttu-id="90754-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90754-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90754-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90754-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90754-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90754-124">INPUTS</span></span>

### <span data-ttu-id="90754-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="90754-125">None</span></span>

## <span data-ttu-id="90754-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90754-126">OUTPUTS</span></span>

### <span data-ttu-id="90754-127">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="90754-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="90754-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90754-128">NOTES</span></span>

## <span data-ttu-id="90754-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90754-129">RELATED LINKS</span></span>

[<span data-ttu-id="90754-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="90754-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)