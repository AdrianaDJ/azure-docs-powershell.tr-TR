---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107761"
---
# <span data-ttu-id="e19e6-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e19e6-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="e19e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e19e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e19e6-103">Belirtilen ön kapı için yeni bir kural Altyapısı yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e19e6-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="e19e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e19e6-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e19e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e19e6-105">DESCRIPTION</span></span>
<span data-ttu-id="e19e6-106">Belirtilen ön kapı için yeni bir kural Altyapısı yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e19e6-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="e19e6-107">Bu cmdlet 'in "-Rules" parametresine geçilecek kural altyapısı kuralları oluşturmak için "New-AzFrontDoorRulesEngineRule" cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e19e6-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="e19e6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e19e6-108">EXAMPLES</span></span>

### <span data-ttu-id="e19e6-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e19e6-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="e19e6-110">Belirtilen ön kapı için yeni bir kural Altyapısı yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e19e6-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="e19e6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e19e6-111">PARAMETERS</span></span>

### <span data-ttu-id="e19e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19e6-112">-DefaultProfile</span></span>
<span data-ttu-id="e19e6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e19e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e19e6-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e19e6-114">-FrontDoorName</span></span>
<span data-ttu-id="e19e6-115">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="e19e6-115">Front Door name.</span></span>

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

### <span data-ttu-id="e19e6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="e19e6-116">-Name</span></span>
<span data-ttu-id="e19e6-117">Kural altyapısı adı.</span><span class="sxs-lookup"><span data-stu-id="e19e6-117">Rules engine name.</span></span>

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

### <span data-ttu-id="e19e6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19e6-118">-ResourceGroupName</span></span>
<span data-ttu-id="e19e6-119">Ön kapıda oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e19e6-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="e19e6-120">-Kural</span><span class="sxs-lookup"><span data-stu-id="e19e6-120">-Rule</span></span>
<span data-ttu-id="e19e6-121">Belirli bir kural altyapısı yapılandırmasını tanımlayan kuralların listesi.</span><span class="sxs-lookup"><span data-stu-id="e19e6-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19e6-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e19e6-122">-Confirm</span></span>
<span data-ttu-id="e19e6-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e19e6-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19e6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e19e6-124">-WhatIf</span></span>
<span data-ttu-id="e19e6-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e19e6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e19e6-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e19e6-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19e6-127">CommonParameters</span></span>
<span data-ttu-id="e19e6-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e19e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19e6-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e19e6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19e6-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e19e6-130">INPUTS</span></span>

### <span data-ttu-id="e19e6-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e19e6-131">None</span></span>

## <span data-ttu-id="e19e6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e19e6-132">OUTPUTS</span></span>

### <span data-ttu-id="e19e6-133">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e19e6-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="e19e6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e19e6-134">NOTES</span></span>

## <span data-ttu-id="e19e6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e19e6-135">RELATED LINKS</span></span>
