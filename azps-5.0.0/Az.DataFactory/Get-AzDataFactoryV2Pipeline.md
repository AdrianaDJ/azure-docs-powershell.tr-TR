---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321001"
---
# <span data-ttu-id="4cb3b-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4cb3b-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="4cb3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb3b-103">Veri Fabrikası içindeki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="4cb3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cb3b-104">SYNTAX</span></span>

### <span data-ttu-id="4cb3b-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4cb3b-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cb3b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4cb3b-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cb3b-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4cb3b-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cb3b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cb3b-108">DESCRIPTION</span></span>
<span data-ttu-id="4cb3b-109">Get-AzDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'ndaki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="4cb3b-110">Bir ardışık düzenin adını belirtirseniz, bu cmdlet bu ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="4cb3b-111">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="4cb3b-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cb3b-112">EXAMPLES</span></span>

### <span data-ttu-id="4cb3b-113">Örnek 1: tüm ardışık düzenler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="4cb3b-113">Example 1: Get information about all pipelines</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="4cb3b-114">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="4cb3b-115">Aşağıdaki örnek komutlardan birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="4cb3b-116">İkincisi bir DataFactory nesnesini parametre olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="4cb3b-117">Örnek 2: belirli bir ardışık düzen hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="4cb3b-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="4cb3b-118">Bu komut, WikiADF adlı veri fabrikası içinde Dpwiöörnek adlı ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="4cb3b-119">Komut bu bilgileri, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4cb3b-120">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="4cb3b-121">Daha fazla bilgi için Get-Help biçim-liste yazın.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="4cb3b-122">Örnek 3: belirli bir ardışık düzenin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="4cb3b-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="4cb3b-123">Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin etkinlikler özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="4cb3b-124">Örnek 4: ilk etkinliğin girişleri hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="4cb3b-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="4cb3b-125">Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin etkinlikler özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="4cb3b-126">Komut, Format-List cmdlet 'ini kullanarak etkinlikler dizisinin ilk öğesinin giriş özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="4cb3b-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cb3b-127">PARAMETERS</span></span>

### <span data-ttu-id="4cb3b-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4cb3b-128">-DataFactory</span></span>
<span data-ttu-id="4cb3b-129">PSDataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="4cb3b-130">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cb3b-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4cb3b-131">-DataFactoryName</span></span>
<span data-ttu-id="4cb3b-132">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4cb3b-133">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cb3b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb3b-134">-DefaultProfile</span></span>
<span data-ttu-id="4cb3b-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cb3b-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cb3b-136">-Name</span></span>
<span data-ttu-id="4cb3b-137">Bilgi alınacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb3b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb3b-138">-ResourceGroupName</span></span>
<span data-ttu-id="4cb3b-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4cb3b-140">Bu cmdlet, bu parametrenin belirttiği gruba ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cb3b-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4cb3b-141">-ResourceId</span></span>
<span data-ttu-id="4cb3b-142">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-142">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb3b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb3b-143">CommonParameters</span></span>
<span data-ttu-id="4cb3b-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cb3b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb3b-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb3b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb3b-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cb3b-146">INPUTS</span></span>

### <span data-ttu-id="4cb3b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4cb3b-147">System.String</span></span>

### <span data-ttu-id="4cb3b-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="4cb3b-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4cb3b-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cb3b-149">OUTPUTS</span></span>

### <span data-ttu-id="4cb3b-150">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="4cb3b-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="4cb3b-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cb3b-151">NOTES</span></span>
<span data-ttu-id="4cb3b-152">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="4cb3b-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4cb3b-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cb3b-153">RELATED LINKS</span></span>

[<span data-ttu-id="4cb3b-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4cb3b-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4cb3b-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4cb3b-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4cb3b-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4cb3b-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
