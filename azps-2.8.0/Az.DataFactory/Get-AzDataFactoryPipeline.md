---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f08d81820ab28688b645ef3ec6a8f519985585c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752554"
---
# <span data-ttu-id="85b7f-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="85b7f-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="85b7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="85b7f-103">Azure Veri Fabrikası 'ndaki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="85b7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85b7f-104">SYNTAX</span></span>

### <span data-ttu-id="85b7f-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="85b7f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85b7f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="85b7f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85b7f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="85b7f-107">DESCRIPTION</span></span>
<span data-ttu-id="85b7f-108">**Get-Azverfactorypypeline** cmdlet, Azure Veri Fabrikası 'ndaki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="85b7f-109">Bir ardışık düzenin adını belirtirseniz, bu cmdlet bu ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="85b7f-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="85b7f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85b7f-111">EXAMPLES</span></span>

### <span data-ttu-id="85b7f-112">Örnek 1: tüm ardışık düzenler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="85b7f-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="85b7f-113">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="85b7f-114">Aşağıdaki örnek komutlardan birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85b7f-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="85b7f-115">İkincisi bir **DataFactory** nesnesini parametre olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="85b7f-116">Örnek 2: belirli bir ardışık düzen hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="85b7f-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="85b7f-117">Bu komut, WikiADF adlı veri fabrikası içinde Dpwiöörnek adlı ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="85b7f-118">Komut bu bilgileri, ardışık düzen işlecini kullanarak Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="85b7f-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="85b7f-119">Bu cmdlet sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="85b7f-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="85b7f-120">Daha fazla bilgi için yazın `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="85b7f-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="85b7f-121">Örnek 3: belirli bir ardışık düzenin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="85b7f-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="85b7f-122">Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin **Özellikler** özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="85b7f-123">Örnek 4: belirli bir ardışık düzenin etkinliklerini alma</span><span class="sxs-lookup"><span data-stu-id="85b7f-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="85b7f-124">Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin **Etkinlikler** özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="85b7f-125">Örnek 5: belirli bir ardışık düzenin çalışma zamanı bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="85b7f-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="85b7f-126">Bu komut, WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzen ile ilişkilendirilmiş **Runtimeınfo** özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="85b7f-127">Örnek 6: ilk etkinliğin girişleri hakkında bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="85b7f-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="85b7f-128">Bu komut WikiADF adlı veri fabrikası içinde Dpwiöen gibi bilgileri alır ve bu ardışık düzene ilişkin **Etkinlikler** özelliğini görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="85b7f-129">Bu komut, **Biçim listesini** kullanarak **Etkinlikler** dizisinin ilk öğesinin **giriş** özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="85b7f-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="85b7f-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85b7f-130">PARAMETERS</span></span>

### <span data-ttu-id="85b7f-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="85b7f-131">-DataFactory</span></span>
<span data-ttu-id="85b7f-132">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b7f-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="85b7f-133">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b7f-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="85b7f-134">-DataFactoryName</span></span>
<span data-ttu-id="85b7f-135">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b7f-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="85b7f-136">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="85b7f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b7f-137">-DefaultProfile</span></span>
<span data-ttu-id="85b7f-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="85b7f-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85b7f-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="85b7f-139">-Name</span></span>
<span data-ttu-id="85b7f-140">Bilgi alınacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b7f-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b7f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b7f-141">-ResourceGroupName</span></span>
<span data-ttu-id="85b7f-142">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b7f-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="85b7f-143">Bu cmdlet, bu parametrenin belirttiği gruba ait ardışık düzenleri alır.</span><span class="sxs-lookup"><span data-stu-id="85b7f-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="85b7f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b7f-144">CommonParameters</span></span>
<span data-ttu-id="85b7f-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85b7f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b7f-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b7f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b7f-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85b7f-147">INPUTS</span></span>

### <span data-ttu-id="85b7f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="85b7f-148">System.String</span></span>

### <span data-ttu-id="85b7f-149">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="85b7f-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="85b7f-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85b7f-150">OUTPUTS</span></span>

### <span data-ttu-id="85b7f-151">Microsoft. Azure. Commands. DataFactory. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="85b7f-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="85b7f-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85b7f-152">NOTES</span></span>
* <span data-ttu-id="85b7f-153">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="85b7f-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="85b7f-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85b7f-154">RELATED LINKS</span></span>

[<span data-ttu-id="85b7f-155">Yeni-Azveri Factorypya</span><span class="sxs-lookup"><span data-stu-id="85b7f-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="85b7f-156">Remove-Azdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="85b7f-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="85b7f-157">Özgeçmiş-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="85b7f-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="85b7f-158">Set-Azdatafactorypipelineactivedönem</span><span class="sxs-lookup"><span data-stu-id="85b7f-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="85b7f-159">Askıya al-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="85b7f-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

