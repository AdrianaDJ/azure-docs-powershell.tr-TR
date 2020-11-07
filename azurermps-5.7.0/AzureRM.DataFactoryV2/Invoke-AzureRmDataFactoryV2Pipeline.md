---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 1503d7307c38c72eece2eb7cb3d6e9f1543be8bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764463"
---
# <span data-ttu-id="05e8d-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="05e8d-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="05e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05e8d-102">SYNOPSIS</span></span>
  <span data-ttu-id="05e8d-103">Bir ardışık düzeni, bir çalıştırmayı başlatmak için çağırır.</span><span class="sxs-lookup"><span data-stu-id="05e8d-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05e8d-104">SYNTAX</span></span>

### <span data-ttu-id="05e8d-105">ByFactoryNameByParameterFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05e8d-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05e8d-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="05e8d-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05e8d-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="05e8d-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05e8d-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="05e8d-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05e8d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="05e8d-109">DESCRIPTION</span></span>
<span data-ttu-id="05e8d-110">**Invoke-AzureRmDataFactoryV2Pipeline** komutu belirtilen ardışık düzene bir çalışma başlatır ve bu çalışma IÇIN bir kimlik döndürür.</span><span class="sxs-lookup"><span data-stu-id="05e8d-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="05e8d-111">Bu GUID, **Get-AzureRmDataFactoryV2PipelineRun** veya **Get-AzureRmDataFactoryV2ActivityRun** 'a bu çalışma hakkında daha fazla ayrıntı almak için iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="05e8d-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="05e8d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05e8d-112">EXAMPLES</span></span>

### <span data-ttu-id="05e8d-113">Örnek 1: bir çalışma başlatmak için ardışık düzen çağırma</span><span class="sxs-lookup"><span data-stu-id="05e8d-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="05e8d-114">Bu komut, "WikiADF" fabrikasında "Dpwisvahili</span><span class="sxs-lookup"><span data-stu-id="05e8d-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="05e8d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05e8d-115">PARAMETERS</span></span>

### <span data-ttu-id="05e8d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="05e8d-116">-DataFactoryName</span></span>
<span data-ttu-id="05e8d-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="05e8d-117">The data factory name.</span></span>

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

### <span data-ttu-id="05e8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e8d-118">-DefaultProfile</span></span>
<span data-ttu-id="05e8d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05e8d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05e8d-120">-InputObject</span></span>
<span data-ttu-id="05e8d-121">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="05e8d-121">The data factory object.</span></span>

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

### <span data-ttu-id="05e8d-122">-Parametre</span><span class="sxs-lookup"><span data-stu-id="05e8d-122">-Parameter</span></span>
<span data-ttu-id="05e8d-123">Ardışık düzen parametreleri.</span><span class="sxs-lookup"><span data-stu-id="05e8d-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="05e8d-124">-Parameterfıle</span><span class="sxs-lookup"><span data-stu-id="05e8d-124">-ParameterFile</span></span>
<span data-ttu-id="05e8d-125">Ardışık düzenin parametrelerini içeren dosyanın adı.</span><span class="sxs-lookup"><span data-stu-id="05e8d-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="05e8d-126">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="05e8d-126">-PipelineName</span></span>
<span data-ttu-id="05e8d-127">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="05e8d-127">The pipeline name.</span></span>

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

### <span data-ttu-id="05e8d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e8d-128">-ResourceGroupName</span></span>
<span data-ttu-id="05e8d-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="05e8d-129">The resource group name.</span></span>

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

### <span data-ttu-id="05e8d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="05e8d-130">-Confirm</span></span>
<span data-ttu-id="05e8d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05e8d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05e8d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e8d-132">-WhatIf</span></span>
<span data-ttu-id="05e8d-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="05e8d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="05e8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e8d-134">CommonParameters</span></span>
<span data-ttu-id="05e8d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05e8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e8d-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e8d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e8d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05e8d-137">INPUTS</span></span>

### <span data-ttu-id="05e8d-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="05e8d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="05e8d-139">System. String System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="05e8d-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="05e8d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05e8d-140">OUTPUTS</span></span>

### <span data-ttu-id="05e8d-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="05e8d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="05e8d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05e8d-142">NOTES</span></span>

## <span data-ttu-id="05e8d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05e8d-143">RELATED LINKS</span></span>

[<span data-ttu-id="05e8d-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="05e8d-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="05e8d-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="05e8d-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

