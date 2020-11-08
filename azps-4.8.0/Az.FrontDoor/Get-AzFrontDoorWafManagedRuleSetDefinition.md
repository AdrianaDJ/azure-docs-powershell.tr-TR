---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274956"
---
# <span data-ttu-id="e19cf-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e19cf-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e19cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e19cf-102">SYNOPSIS</span></span>
<span data-ttu-id="e19cf-103">WAF yönetilen kural kümesi tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="e19cf-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="e19cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e19cf-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e19cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e19cf-105">DESCRIPTION</span></span>
<span data-ttu-id="e19cf-106">WAF yönetilen kural kümesi tanımlarının listesini başvuru olarak kullanılacak şekilde alır</span><span class="sxs-lookup"><span data-stu-id="e19cf-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="e19cf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e19cf-107">EXAMPLES</span></span>

### <span data-ttu-id="e19cf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e19cf-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="e19cf-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="e19cf-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e19cf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e19cf-110">PARAMETERS</span></span>

### <span data-ttu-id="e19cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19cf-111">-DefaultProfile</span></span>
<span data-ttu-id="e19cf-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e19cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e19cf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19cf-113">CommonParameters</span></span>
<span data-ttu-id="e19cf-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e19cf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19cf-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e19cf-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19cf-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e19cf-116">INPUTS</span></span>

### <span data-ttu-id="e19cf-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e19cf-117">None</span></span>

## <span data-ttu-id="e19cf-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e19cf-118">OUTPUTS</span></span>

### <span data-ttu-id="e19cf-119">Microsoft. Azure. Commands. Frontkapısı. modeller. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e19cf-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e19cf-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e19cf-120">NOTES</span></span>

## <span data-ttu-id="e19cf-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e19cf-121">RELATED LINKS</span></span>

<span data-ttu-id="e19cf-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="e19cf-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
