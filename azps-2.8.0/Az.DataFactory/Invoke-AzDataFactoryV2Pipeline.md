---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 5af781170418ea2ab9e0dda9dcd06107e9e784bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752516"
---
# <span data-ttu-id="cf277-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cf277-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="cf277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf277-102">SYNOPSIS</span></span>
  <span data-ttu-id="cf277-103">Bir ardışık düzeni, bir çalıştırmayı başlatmak için çağırır.</span><span class="sxs-lookup"><span data-stu-id="cf277-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="cf277-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf277-104">SYNTAX</span></span>

### <span data-ttu-id="cf277-105">ByFactoryNameByParameterFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf277-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf277-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="cf277-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf277-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="cf277-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf277-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="cf277-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf277-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf277-109">DESCRIPTION</span></span>
<span data-ttu-id="cf277-110">**Invoke-AzDataFactoryV2Pipeline** komutu belirtilen ardışık düzene bir çalışma başlatır ve bu çalışma IÇIN bir kimlik döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf277-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="cf277-111">Bu GUID, **Get-AzDataFactoryV2PipelineRun** veya **Get-AzDataFactoryV2ActivityRun** 'a bu çalışma hakkında daha fazla ayrıntı almak için iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="cf277-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="cf277-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf277-112">EXAMPLES</span></span>

### <span data-ttu-id="cf277-113">Örnek 1: bir çalışma başlatmak için ardışık düzen çağırma</span><span class="sxs-lookup"><span data-stu-id="cf277-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="cf277-114">Bu komut, "WikiADF" fabrikasında "Dpwisvahili</span><span class="sxs-lookup"><span data-stu-id="cf277-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="cf277-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf277-115">PARAMETERS</span></span>

### <span data-ttu-id="cf277-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf277-116">-DataFactoryName</span></span>
<span data-ttu-id="cf277-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="cf277-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf277-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf277-118">-DefaultProfile</span></span>
<span data-ttu-id="cf277-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf277-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf277-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf277-120">-InputObject</span></span>
<span data-ttu-id="cf277-121">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cf277-121">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf277-122">-Parametre</span><span class="sxs-lookup"><span data-stu-id="cf277-122">-Parameter</span></span>
<span data-ttu-id="cf277-123">Ardışık düzen parametreleri.</span><span class="sxs-lookup"><span data-stu-id="cf277-123">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf277-124">-Parameterfıle</span><span class="sxs-lookup"><span data-stu-id="cf277-124">-ParameterFile</span></span>
<span data-ttu-id="cf277-125">Ardışık düzenin parametrelerini içeren dosyanın adı.</span><span class="sxs-lookup"><span data-stu-id="cf277-125">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf277-126">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="cf277-126">-PipelineName</span></span>
<span data-ttu-id="cf277-127">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="cf277-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf277-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf277-128">-ResourceGroupName</span></span>
<span data-ttu-id="cf277-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cf277-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf277-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf277-130">-Confirm</span></span>
<span data-ttu-id="cf277-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf277-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf277-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf277-132">-WhatIf</span></span>
<span data-ttu-id="cf277-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="cf277-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cf277-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf277-134">CommonParameters</span></span>
<span data-ttu-id="cf277-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf277-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf277-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf277-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf277-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf277-137">INPUTS</span></span>

### <span data-ttu-id="cf277-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="cf277-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="cf277-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cf277-139">System.String</span></span>

### <span data-ttu-id="cf277-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cf277-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cf277-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf277-141">OUTPUTS</span></span>

### <span data-ttu-id="cf277-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="cf277-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="cf277-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf277-143">NOTES</span></span>

## <span data-ttu-id="cf277-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf277-144">RELATED LINKS</span></span>

[<span data-ttu-id="cf277-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="cf277-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="cf277-146">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="cf277-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

