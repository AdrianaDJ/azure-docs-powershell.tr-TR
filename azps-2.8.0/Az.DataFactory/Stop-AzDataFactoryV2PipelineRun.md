---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: d055693d9ccb269a747734f490b6a1b47ccf2076
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752424"
---
# <span data-ttu-id="e9ecf-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e9ecf-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="e9ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ecf-103">Veri Fabrikası içinde bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="e9ecf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9ecf-104">SYNTAX</span></span>

### <span data-ttu-id="e9ecf-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e9ecf-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9ecf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e9ecf-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9ecf-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e9ecf-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ecf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9ecf-108">DESCRIPTION</span></span>
<span data-ttu-id="e9ecf-109">**Stop-AzDataFactoryV2PipelineRun** cmdlet 'i, ARDıŞıK düzen kodu ile belirtilen bir veri fabrikası 'nda bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="e9ecf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9ecf-110">EXAMPLES</span></span>

### <span data-ttu-id="e9ecf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e9ecf-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="e9ecf-112">Bu komut, fabrika WikiADF 'de kimliği b9730a13-AA12-4926-a8b3-8e3a974ab0bd olan ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="e9ecf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9ecf-113">PARAMETERS</span></span>

### <span data-ttu-id="e9ecf-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9ecf-114">-DataFactory</span></span>
<span data-ttu-id="e9ecf-115">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-115">The data factory object.</span></span>

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

### <span data-ttu-id="e9ecf-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e9ecf-116">-DataFactoryName</span></span>
<span data-ttu-id="e9ecf-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-117">The data factory name.</span></span>

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

### <span data-ttu-id="e9ecf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ecf-118">-DefaultProfile</span></span>
<span data-ttu-id="e9ecf-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9ecf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9ecf-120">-InputObject</span></span>
<span data-ttu-id="e9ecf-121">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="e9ecf-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e9ecf-122">-PassThru</span></span>
<span data-ttu-id="e9ecf-123">Belirtildiyse, Case 'in cmdlet 'i doğru yazma işlemi başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="e9ecf-124">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="e9ecf-124">-PipelineRunId</span></span>
<span data-ttu-id="e9ecf-125">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="e9ecf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ecf-126">-ResourceGroupName</span></span>
<span data-ttu-id="e9ecf-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-127">The resource group name.</span></span>

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

### <span data-ttu-id="e9ecf-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9ecf-128">-Confirm</span></span>
<span data-ttu-id="e9ecf-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ecf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ecf-130">-WhatIf</span></span>
<span data-ttu-id="e9ecf-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9ecf-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ecf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ecf-133">CommonParameters</span></span>
<span data-ttu-id="e9ecf-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9ecf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ecf-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9ecf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ecf-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9ecf-136">INPUTS</span></span>

### <span data-ttu-id="e9ecf-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="e9ecf-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="e9ecf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e9ecf-138">System.String</span></span>

### <span data-ttu-id="e9ecf-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="e9ecf-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e9ecf-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9ecf-140">OUTPUTS</span></span>

### <span data-ttu-id="e9ecf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9ecf-141">System.Boolean</span></span>

## <span data-ttu-id="e9ecf-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9ecf-142">NOTES</span></span>

## <span data-ttu-id="e9ecf-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9ecf-143">RELATED LINKS</span></span>
