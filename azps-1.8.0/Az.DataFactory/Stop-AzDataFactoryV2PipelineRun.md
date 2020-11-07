---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 3d58b378a64eca438340174d6e2085e26ca3868f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761109"
---
# <span data-ttu-id="e50b1-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e50b1-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="e50b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e50b1-102">SYNOPSIS</span></span>
<span data-ttu-id="e50b1-103">Bir veri fabrikası içinde bir PITe çalışmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e50b1-103">Stops a pieline run in a data factory.</span></span>

## <span data-ttu-id="e50b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e50b1-104">SYNTAX</span></span>

### <span data-ttu-id="e50b1-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e50b1-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e50b1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e50b1-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e50b1-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e50b1-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e50b1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e50b1-108">DESCRIPTION</span></span>
<span data-ttu-id="e50b1-109">**Stop-AzDataFactoryV2PipelineRun** cmdlet 'i, PIELINE Run kimliğiyle belirtilen veri fabrikasında bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="e50b1-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="e50b1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e50b1-110">EXAMPLES</span></span>

### <span data-ttu-id="e50b1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e50b1-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="e50b1-112">Bu komut, fabrika WikiADF 'de kimliği b9730a13-AA12-4926-a8b3-8e3a974ab0bd olan ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="e50b1-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="e50b1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e50b1-113">PARAMETERS</span></span>

### <span data-ttu-id="e50b1-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e50b1-114">-DataFactory</span></span>
<span data-ttu-id="e50b1-115">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e50b1-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e50b1-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e50b1-116">-DataFactoryName</span></span>
<span data-ttu-id="e50b1-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="e50b1-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50b1-118">-DefaultProfile</span></span>
<span data-ttu-id="e50b1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e50b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e50b1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e50b1-120">-InputObject</span></span>
<span data-ttu-id="e50b1-121">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e50b1-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e50b1-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e50b1-122">-PassThru</span></span>
<span data-ttu-id="e50b1-123">Belirtildiyse, Case 'in cmdlet 'i doğru yazma işlemi başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="e50b1-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="e50b1-124">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="e50b1-124">-PipelineRunId</span></span>
<span data-ttu-id="e50b1-125">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e50b1-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50b1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50b1-126">-ResourceGroupName</span></span>
<span data-ttu-id="e50b1-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e50b1-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50b1-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="e50b1-128">-Confirm</span></span>
<span data-ttu-id="e50b1-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e50b1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e50b1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50b1-130">-WhatIf</span></span>
<span data-ttu-id="e50b1-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e50b1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e50b1-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e50b1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e50b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50b1-133">CommonParameters</span></span>
<span data-ttu-id="e50b1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e50b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50b1-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50b1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50b1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e50b1-136">INPUTS</span></span>

### <span data-ttu-id="e50b1-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="e50b1-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="e50b1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e50b1-138">System.String</span></span>

### <span data-ttu-id="e50b1-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="e50b1-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e50b1-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e50b1-140">OUTPUTS</span></span>

### <span data-ttu-id="e50b1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e50b1-141">System.Boolean</span></span>

## <span data-ttu-id="e50b1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e50b1-142">NOTES</span></span>

## <span data-ttu-id="e50b1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e50b1-143">RELATED LINKS</span></span>
