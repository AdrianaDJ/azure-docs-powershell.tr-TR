---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 491d86aa474fb5c392c2d9360657cd1a91072154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752573"
---
# <span data-ttu-id="2fdb4-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="2fdb4-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="2fdb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fdb4-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdb4-103">İş cancelstate durumundaysa devam eden bir databox işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="2fdb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fdb4-104">SYNTAX</span></span>

### <span data-ttu-id="2fdb4-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2fdb4-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fdb4-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2fdb4-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fdb4-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fdb4-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fdb4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fdb4-108">DESCRIPTION</span></span>
<span data-ttu-id="2fdb4-109">Bir databox işini iptal etmek için **stop-AzDataBoxJob** cmdlet 'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="2fdb4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fdb4-110">EXAMPLES</span></span>

### <span data-ttu-id="2fdb4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2fdb4-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="2fdb4-112">Belirtilen databox işini iptal eder</span><span class="sxs-lookup"><span data-stu-id="2fdb4-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="2fdb4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2fdb4-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="2fdb4-114">Belirtilen veri kutusu işini onaysız iptal eder</span><span class="sxs-lookup"><span data-stu-id="2fdb4-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="2fdb4-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2fdb4-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="2fdb4-116">Belirtilen databox işini iptal eder</span><span class="sxs-lookup"><span data-stu-id="2fdb4-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="2fdb4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fdb4-117">PARAMETERS</span></span>

### <span data-ttu-id="2fdb4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdb4-118">-DefaultProfile</span></span>
<span data-ttu-id="2fdb4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fdb4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2fdb4-120">-Force</span></span>
<span data-ttu-id="2fdb4-121">Onaysız durdurma zorla</span><span class="sxs-lookup"><span data-stu-id="2fdb4-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="2fdb4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fdb4-122">-InputObject</span></span>
<span data-ttu-id="2fdb4-123">PSDataBoxJob türünde InputObject</span><span class="sxs-lookup"><span data-stu-id="2fdb4-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="2fdb4-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2fdb4-124">-Name</span></span>
<span data-ttu-id="2fdb4-125">Databox Iş adı</span><span class="sxs-lookup"><span data-stu-id="2fdb4-125">Databox Job Name</span></span>

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

### <span data-ttu-id="2fdb4-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2fdb4-126">-PassThru</span></span>
<span data-ttu-id="2fdb4-127">Geçiş</span><span class="sxs-lookup"><span data-stu-id="2fdb4-127">PassThru</span></span>

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

### <span data-ttu-id="2fdb4-128">-Reason</span><span class="sxs-lookup"><span data-stu-id="2fdb4-128">-Reason</span></span>
<span data-ttu-id="2fdb4-129">Iptal nedeni</span><span class="sxs-lookup"><span data-stu-id="2fdb4-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="2fdb4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdb4-130">-ResourceGroupName</span></span>
<span data-ttu-id="2fdb4-131">Databox Iş kaynağı grubu adı</span><span class="sxs-lookup"><span data-stu-id="2fdb4-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="2fdb4-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2fdb4-132">-ResourceId</span></span>
<span data-ttu-id="2fdb4-133">Veri kutusu kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2fdb4-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="2fdb4-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="2fdb4-134">-Confirm</span></span>
<span data-ttu-id="2fdb4-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdb4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdb4-136">-WhatIf</span></span>
<span data-ttu-id="2fdb4-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fdb4-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdb4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdb4-139">CommonParameters</span></span>
<span data-ttu-id="2fdb4-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdb4-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2fdb4-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdb4-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fdb4-142">INPUTS</span></span>

### <span data-ttu-id="2fdb4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2fdb4-143">System.String</span></span>

## <span data-ttu-id="2fdb4-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fdb4-144">OUTPUTS</span></span>

### <span data-ttu-id="2fdb4-145">System. void</span><span class="sxs-lookup"><span data-stu-id="2fdb4-145">System.Void</span></span>

## <span data-ttu-id="2fdb4-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fdb4-146">NOTES</span></span>

## <span data-ttu-id="2fdb4-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fdb4-147">RELATED LINKS</span></span>