---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764074"
---
# <span data-ttu-id="12716-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="12716-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="12716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12716-102">SYNOPSIS</span></span>
  <span data-ttu-id="12716-103">Bir ardışık düzeni, bir çalıştırmayı başlatmak için çağırır.</span><span class="sxs-lookup"><span data-stu-id="12716-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12716-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12716-104">SYNTAX</span></span>

### <span data-ttu-id="12716-105">ByFactoryNameByParameterFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12716-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="12716-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="12716-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="12716-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="12716-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="12716-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="12716-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="12716-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="12716-109">DESCRIPTION</span></span>
<span data-ttu-id="12716-110">**Invoke-AzureRmDataFactoryV2Pipeline** komutu belirtilen ardışık düzene bir çalışma başlatır ve bu çalışma IÇIN bir kimlik döndürür.</span><span class="sxs-lookup"><span data-stu-id="12716-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="12716-111">Bu GUID, **Get-AzureRmDataFactoryV2PipelineRun** veya **Get-AzureRmDataFactoryV2ActivityRun** 'a bu çalışma hakkında daha fazla ayrıntı almak için iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="12716-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="12716-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12716-112">EXAMPLES</span></span>

### <span data-ttu-id="12716-113">Örnek 1: bir çalışma başlatmak için ardışık düzen çağırma</span><span class="sxs-lookup"><span data-stu-id="12716-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="12716-114">Bu komut, "WikiADF" fabrikasında "Dpwisvahili</span><span class="sxs-lookup"><span data-stu-id="12716-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="12716-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12716-115">PARAMETERS</span></span>

### <span data-ttu-id="12716-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="12716-116">-Confirm</span></span>
<span data-ttu-id="12716-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12716-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12716-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="12716-118">-DataFactoryName</span></span>
<span data-ttu-id="12716-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="12716-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12716-120">-Parameterfıle</span><span class="sxs-lookup"><span data-stu-id="12716-120">-ParameterFile</span></span>
<span data-ttu-id="12716-121">Ardışık düzenin parametrelerini içeren dosyanın adı.</span><span class="sxs-lookup"><span data-stu-id="12716-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12716-122">-Parametre</span><span class="sxs-lookup"><span data-stu-id="12716-122">-Parameter</span></span>
<span data-ttu-id="12716-123">Ardışık düzen parametreleri.</span><span class="sxs-lookup"><span data-stu-id="12716-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12716-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12716-124">-InputObject</span></span>
<span data-ttu-id="12716-125">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="12716-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12716-126">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="12716-126">-PipelineName</span></span>
<span data-ttu-id="12716-127">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="12716-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12716-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12716-128">-ResourceGroupName</span></span>
<span data-ttu-id="12716-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="12716-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12716-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12716-130">-WhatIf</span></span>
<span data-ttu-id="12716-131">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="12716-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="12716-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12716-132">INPUTS</span></span>

### <span data-ttu-id="12716-133">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="12716-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="12716-134">System. String System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="12716-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="12716-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12716-135">OUTPUTS</span></span>

### <span data-ttu-id="12716-136">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="12716-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="12716-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12716-137">NOTES</span></span>

## <span data-ttu-id="12716-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12716-138">RELATED LINKS</span></span>
[<span data-ttu-id="12716-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="12716-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="12716-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="12716-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

