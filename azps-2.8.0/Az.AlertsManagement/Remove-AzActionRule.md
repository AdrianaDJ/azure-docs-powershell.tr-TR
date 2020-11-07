---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 2e0f204fa5eaed80133d699f0381e9116911b581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753660"
---
# <span data-ttu-id="44621-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="44621-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="44621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44621-102">SYNOPSIS</span></span>
<span data-ttu-id="44621-103">Eylem grubunu siler</span><span class="sxs-lookup"><span data-stu-id="44621-103">Deletes a action group</span></span>

## <span data-ttu-id="44621-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44621-104">SYNTAX</span></span>

### <span data-ttu-id="44621-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44621-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44621-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="44621-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44621-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="44621-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44621-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="44621-108">DESCRIPTION</span></span>
<span data-ttu-id="44621-109">**Remove-AzActionRule** cmdlet 'i bir eylem kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="44621-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="44621-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44621-110">EXAMPLES</span></span>

### <span data-ttu-id="44621-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44621-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="44621-112">Bu cmdlet, ad ActionRuleName ile birlikte</span><span class="sxs-lookup"><span data-stu-id="44621-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="44621-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44621-113">PARAMETERS</span></span>

### <span data-ttu-id="44621-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44621-114">-DefaultProfile</span></span>
<span data-ttu-id="44621-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44621-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44621-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44621-116">-InputObject</span></span>
<span data-ttu-id="44621-117">Eylem kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="44621-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44621-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="44621-118">-Name</span></span>
<span data-ttu-id="44621-119">Eylem kuralının adı</span><span class="sxs-lookup"><span data-stu-id="44621-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44621-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="44621-120">-PassThru</span></span>
<span data-ttu-id="44621-121">Geçiş, çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="44621-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="44621-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="44621-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44621-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44621-123">-ResourceGroupName</span></span>
<span data-ttu-id="44621-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="44621-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44621-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="44621-125">-ResourceId</span></span>
<span data-ttu-id="44621-126">Kaynak No 'dan eylem kuralı alın.</span><span class="sxs-lookup"><span data-stu-id="44621-126">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44621-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="44621-127">-Confirm</span></span>
<span data-ttu-id="44621-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="44621-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44621-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44621-129">-WhatIf</span></span>
<span data-ttu-id="44621-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44621-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44621-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="44621-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44621-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44621-132">CommonParameters</span></span>
<span data-ttu-id="44621-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44621-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44621-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="44621-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44621-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44621-135">INPUTS</span></span>

### <span data-ttu-id="44621-136">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="44621-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="44621-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44621-137">OUTPUTS</span></span>

### <span data-ttu-id="44621-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44621-138">System.Boolean</span></span>

## <span data-ttu-id="44621-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44621-139">NOTES</span></span>

## <span data-ttu-id="44621-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44621-140">RELATED LINKS</span></span>
