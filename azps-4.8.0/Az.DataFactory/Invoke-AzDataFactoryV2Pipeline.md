---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275039"
---
# <span data-ttu-id="30162-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="30162-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="30162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30162-102">SYNOPSIS</span></span>
  <span data-ttu-id="30162-103">Bir ardışık düzeni, bir çalıştırmayı başlatmak için çağırır.</span><span class="sxs-lookup"><span data-stu-id="30162-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="30162-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30162-104">SYNTAX</span></span>

### <span data-ttu-id="30162-105">ByFactoryNameByParameterFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30162-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30162-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="30162-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30162-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="30162-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30162-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="30162-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30162-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="30162-109">DESCRIPTION</span></span>
<span data-ttu-id="30162-110">**Invoke-AzDataFactoryV2Pipeline** komutu belirtilen ardışık düzene bir çalışma başlatır ve bu çalışma IÇIN bir kimlik döndürür.</span><span class="sxs-lookup"><span data-stu-id="30162-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="30162-111">Bu GUID, **Get-AzDataFactoryV2PipelineRun** veya **Get-AzDataFactoryV2ActivityRun** 'a bu çalışma hakkında daha fazla ayrıntı almak için iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="30162-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="30162-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30162-112">EXAMPLES</span></span>

### <span data-ttu-id="30162-113">Örnek 1: bir çalışma başlatmak için ardışık düzen çağırma</span><span class="sxs-lookup"><span data-stu-id="30162-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="30162-114">Bu komut, "WikiADF" fabrikasında "Dpwisvahili</span><span class="sxs-lookup"><span data-stu-id="30162-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="30162-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="30162-115">Example 2</span></span>

<span data-ttu-id="30162-116">Bir ardışık düzeni, bir çalıştırmayı başlatmak için çağırır.</span><span class="sxs-lookup"><span data-stu-id="30162-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="30162-117">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="30162-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="30162-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30162-118">PARAMETERS</span></span>

### <span data-ttu-id="30162-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="30162-119">-DataFactoryName</span></span>
<span data-ttu-id="30162-120">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="30162-120">The data factory name.</span></span>

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

### <span data-ttu-id="30162-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30162-121">-DefaultProfile</span></span>
<span data-ttu-id="30162-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30162-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30162-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30162-123">-InputObject</span></span>
<span data-ttu-id="30162-124">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="30162-124">The data factory object.</span></span>

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

### <span data-ttu-id="30162-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="30162-125">-IsRecovery</span></span>
<span data-ttu-id="30162-126">Kurtarma modu bayrağı.</span><span class="sxs-lookup"><span data-stu-id="30162-126">Recovery mode flag.</span></span> <span data-ttu-id="30162-127">Kurtarma modu true olarak ayarlandıysa, belirtilen başvurulan ardışık düzen çalışır ve yeni çalışma aynı GroupID altında gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="30162-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30162-128">-Parametre</span><span class="sxs-lookup"><span data-stu-id="30162-128">-Parameter</span></span>
<span data-ttu-id="30162-129">Ardışık düzen parametreleri.</span><span class="sxs-lookup"><span data-stu-id="30162-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="30162-130">-Parameterfıle</span><span class="sxs-lookup"><span data-stu-id="30162-130">-ParameterFile</span></span>
<span data-ttu-id="30162-131">Ardışık düzenin parametrelerini içeren dosyanın adı.</span><span class="sxs-lookup"><span data-stu-id="30162-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="30162-132">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="30162-132">-PipelineName</span></span>
<span data-ttu-id="30162-133">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="30162-133">The pipeline name.</span></span>

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

### <span data-ttu-id="30162-134">-Referencepipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="30162-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="30162-135">Yeniden çalıştırma için ardışık düzen kodu.</span><span class="sxs-lookup"><span data-stu-id="30162-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="30162-136">Run ID belirtildiyse, belirtilen Run parametreleri yeni bir çalışma oluşturmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="30162-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30162-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30162-137">-ResourceGroupName</span></span>
<span data-ttu-id="30162-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="30162-138">The resource group name.</span></span>

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

### <span data-ttu-id="30162-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="30162-139">-StartActivityName</span></span>
<span data-ttu-id="30162-140">Kurtarma modunda, yeniden çalıştırma bu aktiviteden başlar.</span><span class="sxs-lookup"><span data-stu-id="30162-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="30162-141">Belirtilmemişse tüm etkinlikler çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="30162-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30162-142">-Startfromhatası</span><span class="sxs-lookup"><span data-stu-id="30162-142">-StartFromFailure</span></span>
<span data-ttu-id="30162-143">Başarısız etkinlikler bayrağını yeniden çalıştır bayrağını başlatın.</span><span class="sxs-lookup"><span data-stu-id="30162-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="30162-144">Kurtarma modunda belirtilmişse, yeniden çalıştırma işlemi başarısız etkinliklerden başlar.</span><span class="sxs-lookup"><span data-stu-id="30162-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30162-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="30162-145">-Confirm</span></span>
<span data-ttu-id="30162-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30162-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30162-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30162-147">-WhatIf</span></span>
<span data-ttu-id="30162-148">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="30162-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="30162-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30162-149">CommonParameters</span></span>
<span data-ttu-id="30162-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30162-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30162-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30162-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30162-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30162-152">INPUTS</span></span>

### <span data-ttu-id="30162-153">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="30162-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="30162-154">System. String</span><span class="sxs-lookup"><span data-stu-id="30162-154">System.String</span></span>

### <span data-ttu-id="30162-155">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="30162-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30162-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30162-156">OUTPUTS</span></span>

### <span data-ttu-id="30162-157">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="30162-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="30162-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30162-158">NOTES</span></span>

## <span data-ttu-id="30162-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30162-159">RELATED LINKS</span></span>

[<span data-ttu-id="30162-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="30162-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="30162-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="30162-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

