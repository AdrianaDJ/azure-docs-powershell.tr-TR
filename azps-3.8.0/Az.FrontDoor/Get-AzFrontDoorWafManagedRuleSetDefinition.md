---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937486"
---
# <span data-ttu-id="501bf-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="501bf-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="501bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="501bf-102">SYNOPSIS</span></span>
<span data-ttu-id="501bf-103">WAF yönetilen kural kümesi tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="501bf-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="501bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="501bf-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="501bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="501bf-105">DESCRIPTION</span></span>
<span data-ttu-id="501bf-106">WAF yönetilen kural kümesi tanımlarının listesini başvuru olarak kullanılacak şekilde alır</span><span class="sxs-lookup"><span data-stu-id="501bf-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="501bf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="501bf-107">EXAMPLES</span></span>

### <span data-ttu-id="501bf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="501bf-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="501bf-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="501bf-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="501bf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="501bf-110">PARAMETERS</span></span>

### <span data-ttu-id="501bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501bf-111">-DefaultProfile</span></span>
<span data-ttu-id="501bf-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="501bf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="501bf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501bf-113">CommonParameters</span></span>
<span data-ttu-id="501bf-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="501bf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501bf-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="501bf-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501bf-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="501bf-116">INPUTS</span></span>

### <span data-ttu-id="501bf-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="501bf-117">None</span></span>

## <span data-ttu-id="501bf-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="501bf-118">OUTPUTS</span></span>

### <span data-ttu-id="501bf-119">Microsoft. Azure. Commands. Frontkapısı. modeller. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="501bf-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="501bf-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="501bf-120">NOTES</span></span>

## <span data-ttu-id="501bf-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="501bf-121">RELATED LINKS</span></span>

<span data-ttu-id="501bf-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="501bf-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
