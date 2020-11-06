---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572754"
---
# <span data-ttu-id="e04c1-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="e04c1-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="e04c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e04c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e04c1-103">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e04c1-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e04c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e04c1-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e04c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e04c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e04c1-106">WAF ilkesi oluşturma için RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e04c1-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="e04c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e04c1-107">EXAMPLES</span></span>

### <span data-ttu-id="e04c1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e04c1-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="e04c1-109">RuleGroupOverride nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e04c1-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="e04c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e04c1-110">PARAMETERS</span></span>

### <span data-ttu-id="e04c1-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="e04c1-111">-Action</span></span>
<span data-ttu-id="e04c1-112">Eylem türü.</span><span class="sxs-lookup"><span data-stu-id="e04c1-112">Type of Actions.</span></span>
<span data-ttu-id="e04c1-113">Olası değerler: ' Izin ver ', ' engelle ', ' günlük '</span><span class="sxs-lookup"><span data-stu-id="e04c1-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04c1-114">-DefaultProfile</span></span>
<span data-ttu-id="e04c1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e04c1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04c1-116">-Geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="e04c1-116">-Override</span></span>
<span data-ttu-id="e04c1-117">Overderulegroup.</span><span class="sxs-lookup"><span data-stu-id="e04c1-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="e04c1-118">Olası değerler: ' SqlInjection ', ' XSS '</span><span class="sxs-lookup"><span data-stu-id="e04c1-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04c1-119">CommonParameters</span></span>
<span data-ttu-id="e04c1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e04c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04c1-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04c1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04c1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e04c1-122">INPUTS</span></span>

### <span data-ttu-id="e04c1-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e04c1-123">None</span></span>

## <span data-ttu-id="e04c1-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e04c1-124">OUTPUTS</span></span>

### <span data-ttu-id="e04c1-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e04c1-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="e04c1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e04c1-126">NOTES</span></span>

## <span data-ttu-id="e04c1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e04c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="e04c1-128">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e04c1-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
