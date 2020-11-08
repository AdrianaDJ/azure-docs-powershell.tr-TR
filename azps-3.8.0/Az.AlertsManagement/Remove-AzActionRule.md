---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 1cdea9a2d5deb9fbe93da0a090070f7ed1b07653
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096675"
---
# <span data-ttu-id="acf88-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="acf88-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="acf88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acf88-102">SYNOPSIS</span></span>
<span data-ttu-id="acf88-103">Eylem kuralı silme</span><span class="sxs-lookup"><span data-stu-id="acf88-103">Deletes a action rule</span></span>

## <span data-ttu-id="acf88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acf88-104">SYNTAX</span></span>

### <span data-ttu-id="acf88-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="acf88-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf88-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="acf88-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf88-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="acf88-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf88-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="acf88-108">DESCRIPTION</span></span>
<span data-ttu-id="acf88-109">**Remove-AzActionRule** cmdlet 'i bir eylem kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="acf88-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="acf88-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acf88-110">EXAMPLES</span></span>

### <span data-ttu-id="acf88-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="acf88-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="acf88-112">Bu cmdlet, ad ActionRuleName ile birlikte</span><span class="sxs-lookup"><span data-stu-id="acf88-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="acf88-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acf88-113">PARAMETERS</span></span>

### <span data-ttu-id="acf88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf88-114">-DefaultProfile</span></span>
<span data-ttu-id="acf88-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="acf88-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf88-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf88-116">-InputObject</span></span>
<span data-ttu-id="acf88-117">Eylem kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="acf88-117">The action rule resource</span></span>

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

### <span data-ttu-id="acf88-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="acf88-118">-Name</span></span>
<span data-ttu-id="acf88-119">Eylem kuralının adı</span><span class="sxs-lookup"><span data-stu-id="acf88-119">Name of action rule</span></span>

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

### <span data-ttu-id="acf88-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="acf88-120">-PassThru</span></span>
<span data-ttu-id="acf88-121">Geçiş, çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="acf88-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="acf88-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="acf88-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="acf88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf88-123">-ResourceGroupName</span></span>
<span data-ttu-id="acf88-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="acf88-124">Resource Group name</span></span>

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

### <span data-ttu-id="acf88-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="acf88-125">-ResourceId</span></span>
<span data-ttu-id="acf88-126">Kaynak No 'dan eylem kuralı alın.</span><span class="sxs-lookup"><span data-stu-id="acf88-126">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="acf88-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="acf88-127">-Confirm</span></span>
<span data-ttu-id="acf88-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acf88-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf88-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf88-129">-WhatIf</span></span>
<span data-ttu-id="acf88-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acf88-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf88-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acf88-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf88-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf88-132">CommonParameters</span></span>
<span data-ttu-id="acf88-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acf88-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf88-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="acf88-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf88-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acf88-135">INPUTS</span></span>

### <span data-ttu-id="acf88-136">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="acf88-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="acf88-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acf88-137">OUTPUTS</span></span>

### <span data-ttu-id="acf88-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="acf88-138">System.Boolean</span></span>

## <span data-ttu-id="acf88-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acf88-139">NOTES</span></span>

## <span data-ttu-id="acf88-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acf88-140">RELATED LINKS</span></span>
