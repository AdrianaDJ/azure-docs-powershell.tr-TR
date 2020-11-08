---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938267"
---
# <span data-ttu-id="12075-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="12075-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="12075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12075-102">SYNOPSIS</span></span>
<span data-ttu-id="12075-103">Veri Fabrikası içinde bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="12075-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="12075-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12075-104">SYNTAX</span></span>

### <span data-ttu-id="12075-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12075-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12075-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12075-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12075-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="12075-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12075-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="12075-108">DESCRIPTION</span></span>
<span data-ttu-id="12075-109">**Stop-AzDataFactoryV2PipelineRun** cmdlet 'i, ARDıŞıK düzen kodu ile belirtilen bir veri fabrikası 'nda bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="12075-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="12075-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12075-110">EXAMPLES</span></span>

### <span data-ttu-id="12075-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="12075-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="12075-112">Bu komut, fabrika WikiADF 'de kimliği b9730a13-AA12-4926-a8b3-8e3a974ab0bd olan ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="12075-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="12075-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12075-113">PARAMETERS</span></span>

### <span data-ttu-id="12075-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="12075-114">-DataFactory</span></span>
<span data-ttu-id="12075-115">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="12075-115">The data factory object.</span></span>

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

### <span data-ttu-id="12075-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="12075-116">-DataFactoryName</span></span>
<span data-ttu-id="12075-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="12075-117">The data factory name.</span></span>

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

### <span data-ttu-id="12075-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12075-118">-DefaultProfile</span></span>
<span data-ttu-id="12075-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12075-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12075-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12075-120">-InputObject</span></span>
<span data-ttu-id="12075-121">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="12075-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="12075-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="12075-122">-PassThru</span></span>
<span data-ttu-id="12075-123">Belirtildiyse, Case 'in cmdlet 'i doğru yazma işlemi başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="12075-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="12075-124">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="12075-124">-PipelineRunId</span></span>
<span data-ttu-id="12075-125">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="12075-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="12075-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12075-126">-ResourceGroupName</span></span>
<span data-ttu-id="12075-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="12075-127">The resource group name.</span></span>

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

### <span data-ttu-id="12075-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="12075-128">-Confirm</span></span>
<span data-ttu-id="12075-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12075-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12075-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12075-130">-WhatIf</span></span>
<span data-ttu-id="12075-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12075-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12075-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12075-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12075-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12075-133">CommonParameters</span></span>
<span data-ttu-id="12075-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12075-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12075-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12075-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12075-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12075-136">INPUTS</span></span>

### <span data-ttu-id="12075-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="12075-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="12075-138">System. String</span><span class="sxs-lookup"><span data-stu-id="12075-138">System.String</span></span>

### <span data-ttu-id="12075-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="12075-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="12075-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12075-140">OUTPUTS</span></span>

### <span data-ttu-id="12075-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12075-141">System.Boolean</span></span>

## <span data-ttu-id="12075-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12075-142">NOTES</span></span>

## <span data-ttu-id="12075-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12075-143">RELATED LINKS</span></span>