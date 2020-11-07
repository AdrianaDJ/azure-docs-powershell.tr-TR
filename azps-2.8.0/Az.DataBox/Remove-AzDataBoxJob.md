---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 76796f86c69cbb9fa24765da8ebf8ed5bd9c1da8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752575"
---
# <span data-ttu-id="02540-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="02540-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="02540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02540-102">SYNOPSIS</span></span>
<span data-ttu-id="02540-103">Databox işini siler</span><span class="sxs-lookup"><span data-stu-id="02540-103">Deletes the databox job</span></span>

## <span data-ttu-id="02540-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02540-104">SYNTAX</span></span>

### <span data-ttu-id="02540-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02540-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02540-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="02540-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02540-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02540-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02540-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="02540-108">DESCRIPTION</span></span>
<span data-ttu-id="02540-109">**Remove-AzDataBoxJob** cmdlet 'i, veri kutusu işleri listesinden tamamlanmış bir veri kutusu işini silmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="02540-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="02540-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02540-110">EXAMPLES</span></span>

### <span data-ttu-id="02540-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02540-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="02540-112">Belirtilen databox işini siler</span><span class="sxs-lookup"><span data-stu-id="02540-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="02540-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="02540-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="02540-114">Belirtilen veri kutusu işini onaysız olarak silme</span><span class="sxs-lookup"><span data-stu-id="02540-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="02540-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="02540-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="02540-116">Belirtilen databox işini siler</span><span class="sxs-lookup"><span data-stu-id="02540-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="02540-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02540-117">PARAMETERS</span></span>

### <span data-ttu-id="02540-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02540-118">-DefaultProfile</span></span>
<span data-ttu-id="02540-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02540-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02540-120">-Force</span><span class="sxs-lookup"><span data-stu-id="02540-120">-Force</span></span>
<span data-ttu-id="02540-121">Onaysız kaldırmaya zorla</span><span class="sxs-lookup"><span data-stu-id="02540-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="02540-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02540-122">-InputObject</span></span>
<span data-ttu-id="02540-123">PSDataBoxJob türünde InputObject</span><span class="sxs-lookup"><span data-stu-id="02540-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02540-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="02540-124">-Name</span></span>
<span data-ttu-id="02540-125">Databox Iş adı</span><span class="sxs-lookup"><span data-stu-id="02540-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02540-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02540-126">-PassThru</span></span>
<span data-ttu-id="02540-127">Geçiş</span><span class="sxs-lookup"><span data-stu-id="02540-127">PassThru</span></span>

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

### <span data-ttu-id="02540-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02540-128">-ResourceGroupName</span></span>
<span data-ttu-id="02540-129">Databox Iş kaynağı grubu adı</span><span class="sxs-lookup"><span data-stu-id="02540-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02540-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02540-130">-ResourceId</span></span>
<span data-ttu-id="02540-131">Databox Iş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="02540-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02540-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="02540-132">-Confirm</span></span>
<span data-ttu-id="02540-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02540-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02540-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02540-134">-WhatIf</span></span>
<span data-ttu-id="02540-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02540-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02540-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02540-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02540-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02540-137">CommonParameters</span></span>
<span data-ttu-id="02540-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02540-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02540-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02540-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02540-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02540-140">INPUTS</span></span>

### <span data-ttu-id="02540-141">System. String</span><span class="sxs-lookup"><span data-stu-id="02540-141">System.String</span></span>

## <span data-ttu-id="02540-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02540-142">OUTPUTS</span></span>

### <span data-ttu-id="02540-143">System. void</span><span class="sxs-lookup"><span data-stu-id="02540-143">System.Void</span></span>

## <span data-ttu-id="02540-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02540-144">NOTES</span></span>

## <span data-ttu-id="02540-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02540-145">RELATED LINKS</span></span>
