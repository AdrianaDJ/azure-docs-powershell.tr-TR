---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: b8065c3b4aa958c9138316488b7ca8a9b982d97c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594748"
---
# <span data-ttu-id="e7900-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e7900-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e7900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7900-102">SYNOPSIS</span></span>
<span data-ttu-id="e7900-103">Veri Fabrikası içindeki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7900-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7900-104">SYNTAX</span></span>

### <span data-ttu-id="e7900-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7900-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="e7900-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e7900-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="e7900-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7900-107">DESCRIPTION</span></span>
<span data-ttu-id="e7900-108">Get-AzureRmDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'ndaki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="e7900-109">Bir ardışık düzenin adını belirtirseniz, bu cmdlet bu ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="e7900-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="e7900-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7900-111">EXAMPLES</span></span>

### <span data-ttu-id="e7900-112">Örnek 1: tüm ardışık düzenler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="e7900-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="e7900-113">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="e7900-114">Aşağıdaki örnek komutlardan birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7900-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="e7900-115">İkincisi bir DataFactory nesnesini parametre olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="e7900-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="e7900-116">Örnek 2: belirli bir ardışık düzen hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="e7900-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="e7900-117">Bu komut, WikiADF adlı veri fabrikası içinde Dpwiöörnek adlı ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="e7900-118">Komut bu bilgileri, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="e7900-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e7900-119">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="e7900-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="e7900-120">Daha fazla bilgi için Get-Help biçim-liste yazın.</span><span class="sxs-lookup"><span data-stu-id="e7900-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="e7900-121">Örnek 3: belirli bir ardışık düzenin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="e7900-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}

```

<span data-ttu-id="e7900-122">Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin etkinlikler özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e7900-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="e7900-123">Örnek 6: ilk etkinliğin girişleri hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="e7900-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :

```

<span data-ttu-id="e7900-124">Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin etkinlikler özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e7900-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="e7900-125">Komut, Format-List cmdlet 'ini kullanarak etkinlikler dizisinin ilk öğesinin giriş özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e7900-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="e7900-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7900-126">PARAMETERS</span></span>

### <span data-ttu-id="e7900-127">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e7900-127">-DataFactory</span></span>
<span data-ttu-id="e7900-128">PSDataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7900-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="e7900-129">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7900-130">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e7900-130">-DataFactoryName</span></span>
<span data-ttu-id="e7900-131">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7900-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e7900-132">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e7900-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7900-133">-Name</span></span>
<span data-ttu-id="e7900-134">Bilgi alınacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7900-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7900-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7900-135">-ResourceGroupName</span></span>
<span data-ttu-id="e7900-136">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7900-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e7900-137">Bu cmdlet, bu parametrenin belirttiği gruba ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="e7900-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="e7900-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7900-138">INPUTS</span></span>

### <span data-ttu-id="e7900-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e7900-139">System.String</span></span>
<span data-ttu-id="e7900-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="e7900-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="e7900-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7900-141">OUTPUTS</span></span>

### <span data-ttu-id="e7900-142">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e7900-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e7900-143">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e7900-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="e7900-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7900-144">NOTES</span></span>
<span data-ttu-id="e7900-145">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="e7900-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e7900-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7900-146">RELATED LINKS</span></span>
[<span data-ttu-id="e7900-147">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e7900-147">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e7900-148">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e7900-148">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e7900-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e7900-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
