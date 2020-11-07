---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2a936b9a75e9fc1053e2202950a6a6b4c49bd3a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765186"
---
# <span data-ttu-id="8099d-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8099d-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8099d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8099d-102">SYNOPSIS</span></span>
<span data-ttu-id="8099d-103">Veri Fabrikası içinde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8099d-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8099d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8099d-104">SYNTAX</span></span>

### <span data-ttu-id="8099d-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8099d-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8099d-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8099d-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="8099d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8099d-107">DESCRIPTION</span></span>
<span data-ttu-id="8099d-108">Set-AzureRmDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'nde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8099d-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="8099d-109">Önceden var olan bir ardışık düzen için ad belirtirseniz, cmdlet, ardışık düzeni değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="8099d-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="8099d-110">Force parametresini belirtirseniz, cmdlet mevcut ardışık düzenin yerine geçer.</span><span class="sxs-lookup"><span data-stu-id="8099d-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="8099d-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="8099d-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="8099d-112">Veri Fabrikası içinde aynı ada sahip bir ardışık düzen varsa, bu cmdlet yeni ardışık düzenin mevcut ardışık düzenin üzerine yazılıp yazılmayacağını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8099d-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="8099d-113">Mevcut ardışık düzenin üzerine yazılmasını onaylamıyorsanız, ardışık düzen tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="8099d-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="8099d-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8099d-114">EXAMPLES</span></span>

### <span data-ttu-id="8099d-115">Örnek 1: ardışık düzen oluşturma</span><span class="sxs-lookup"><span data-stu-id="8099d-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="8099d-116">Bu komut, ADF adlı veri fabrikası içinde Dpwiöörnek adlı bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8099d-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="8099d-117">Komut, ardışık düzeni DPWikisample.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="8099d-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="8099d-118">Bu dosya, ardışık düzene kopyalama etkinliği ve HDInsight etkinliği gibi etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="8099d-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="8099d-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8099d-119">PARAMETERS</span></span>

### <span data-ttu-id="8099d-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="8099d-120">-Confirm</span></span>
<span data-ttu-id="8099d-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8099d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8099d-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8099d-122">-DataFactoryName</span></span>
<span data-ttu-id="8099d-123">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8099d-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8099d-124">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8099d-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8099d-125">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="8099d-125">-DefinitionFile</span></span>
<span data-ttu-id="8099d-126">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="8099d-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8099d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8099d-127">-Force</span></span>
<span data-ttu-id="8099d-128">Bu cmdlet 'in mevcut bir ardışık düzeni sizden onay istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8099d-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8099d-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="8099d-129">-Name</span></span>
<span data-ttu-id="8099d-130">Oluşturulacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8099d-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8099d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8099d-131">-ResourceGroupName</span></span>
<span data-ttu-id="8099d-132">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8099d-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8099d-133">Bu cmdlet, bu parametrenin belirttiği grup için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8099d-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8099d-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8099d-134">-ResourceId</span></span>
<span data-ttu-id="8099d-135">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8099d-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8099d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8099d-136">-WhatIf</span></span>
<span data-ttu-id="8099d-137">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="8099d-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="8099d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8099d-138">INPUTS</span></span>

### <span data-ttu-id="8099d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8099d-139">System.String</span></span>


## <span data-ttu-id="8099d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8099d-140">OUTPUTS</span></span>

### <span data-ttu-id="8099d-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8099d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="8099d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8099d-142">NOTES</span></span>
<span data-ttu-id="8099d-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="8099d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8099d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8099d-144">RELATED LINKS</span></span>
[<span data-ttu-id="8099d-145">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8099d-145">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8099d-146">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8099d-146">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8099d-147">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8099d-147">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
