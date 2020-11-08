---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275440"
---
# <span data-ttu-id="9ee37-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="9ee37-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="9ee37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee37-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee37-103">Kural motorunu ön kapıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="9ee37-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="9ee37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ee37-104">SYNTAX</span></span>

### <span data-ttu-id="9ee37-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ee37-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee37-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ee37-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ee37-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9ee37-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ee37-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ee37-108">DESCRIPTION</span></span>
<span data-ttu-id="9ee37-109">Kural motorunu ön kapıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="9ee37-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="9ee37-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ee37-110">EXAMPLES</span></span>

### <span data-ttu-id="9ee37-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ee37-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="9ee37-112">Kural altyapısı yapılandırmasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="9ee37-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="9ee37-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9ee37-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="9ee37-114">Varolmayan bir kural Altyapısı yapılandırması kaldırılırken beklenen sonuç.</span><span class="sxs-lookup"><span data-stu-id="9ee37-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="9ee37-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ee37-115">PARAMETERS</span></span>

### <span data-ttu-id="9ee37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee37-116">-DefaultProfile</span></span>
<span data-ttu-id="9ee37-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ee37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee37-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="9ee37-118">-FrontDoorName</span></span>
<span data-ttu-id="9ee37-119">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="9ee37-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee37-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ee37-120">-InputObject</span></span>
<span data-ttu-id="9ee37-121">Güncelleştirilecek kural altyapısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9ee37-121">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee37-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ee37-122">-Name</span></span>
<span data-ttu-id="9ee37-123">Kural altyapısı adı.</span><span class="sxs-lookup"><span data-stu-id="9ee37-123">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee37-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9ee37-124">-PassThru</span></span>
<span data-ttu-id="9ee37-125">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="9ee37-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="9ee37-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee37-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ee37-127">Ön kapıda oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9ee37-127">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee37-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9ee37-128">-ResourceId</span></span>
<span data-ttu-id="9ee37-129">Güncelleştirilecek RulesEngine kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9ee37-129">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee37-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ee37-130">-Confirm</span></span>
<span data-ttu-id="9ee37-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ee37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ee37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee37-132">-WhatIf</span></span>
<span data-ttu-id="9ee37-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ee37-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ee37-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ee37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ee37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee37-135">CommonParameters</span></span>
<span data-ttu-id="9ee37-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ee37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee37-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ee37-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee37-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ee37-138">INPUTS</span></span>

### <span data-ttu-id="9ee37-139">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="9ee37-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="9ee37-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9ee37-140">System.String</span></span>

## <span data-ttu-id="9ee37-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ee37-141">OUTPUTS</span></span>

### <span data-ttu-id="9ee37-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ee37-142">System.Boolean</span></span>

## <span data-ttu-id="9ee37-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ee37-143">NOTES</span></span>

## <span data-ttu-id="9ee37-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ee37-144">RELATED LINKS</span></span>
