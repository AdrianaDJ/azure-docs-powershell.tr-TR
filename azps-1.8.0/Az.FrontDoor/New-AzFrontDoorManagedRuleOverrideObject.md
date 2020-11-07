---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
ms.openlocfilehash: e45abaae34f3b8449920dad122736c46b9d946ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916719"
---
# <span data-ttu-id="4dca9-101">New-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="4dca9-101">New-AzFrontDoorManagedRuleOverrideObject</span></span>

## <span data-ttu-id="4dca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dca9-102">SYNOPSIS</span></span>
<span data-ttu-id="4dca9-103">Yönetilen kural geçersiz kılma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4dca9-103">Create managed rule override object</span></span>

## <span data-ttu-id="4dca9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4dca9-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleOverrideObject -RuleId <String> [-Action <PSAction>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dca9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4dca9-105">DESCRIPTION</span></span>
<span data-ttu-id="4dca9-106">Yönetilen WAF kural grubu için PSAzureManagedRuleOverride nesnesi oluşturma nesne oluşturma.</span><span class="sxs-lookup"><span data-stu-id="4dca9-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="4dca9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4dca9-107">EXAMPLES</span></span>

### <span data-ttu-id="4dca9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4dca9-108">Example 1</span></span>
<span data-ttu-id="4dca9-109">942250 kuralı için yönetilen kural geçersiz kılma nesnesi oluşturun (SQLı grubunda).</span><span class="sxs-lookup"><span data-stu-id="4dca9-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="4dca9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4dca9-110">PARAMETERS</span></span>

### <span data-ttu-id="4dca9-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="4dca9-111">-Action</span></span>
<span data-ttu-id="4dca9-112">Geçersiz kılma eylemi</span><span class="sxs-lookup"><span data-stu-id="4dca9-112">Override Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dca9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dca9-113">-DefaultProfile</span></span>
<span data-ttu-id="4dca9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4dca9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dca9-115">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="4dca9-115">-Disabled</span></span>
<span data-ttu-id="4dca9-116">Devre dışı durumu</span><span class="sxs-lookup"><span data-stu-id="4dca9-116">Disabled state</span></span>

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

### <span data-ttu-id="4dca9-117">-RuleId</span><span class="sxs-lookup"><span data-stu-id="4dca9-117">-RuleId</span></span>
<span data-ttu-id="4dca9-118">Kural KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="4dca9-118">Rule ID</span></span>

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

### <span data-ttu-id="4dca9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dca9-119">CommonParameters</span></span>
<span data-ttu-id="4dca9-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4dca9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dca9-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4dca9-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dca9-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4dca9-122">INPUTS</span></span>

### <span data-ttu-id="4dca9-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4dca9-123">None</span></span>

## <span data-ttu-id="4dca9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4dca9-124">OUTPUTS</span></span>

### <span data-ttu-id="4dca9-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4dca9-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="4dca9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4dca9-126">NOTES</span></span>

## <span data-ttu-id="4dca9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4dca9-127">RELATED LINKS</span></span>

[<span data-ttu-id="4dca9-128">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="4dca9-128">New-AzFrontDoorRuleGroupOverrideObject</span></span>](./New-AzFrontDoorRuleGroupOverrideObject.md)