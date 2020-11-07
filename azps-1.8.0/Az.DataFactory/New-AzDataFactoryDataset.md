---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 1d03ba1e4b025be933fd9cd409270d8deb93d1d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761144"
---
# <span data-ttu-id="d2eb7-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d2eb7-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="d2eb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="d2eb7-103">Veri Fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="d2eb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2eb7-104">SYNTAX</span></span>

### <span data-ttu-id="d2eb7-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2eb7-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2eb7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d2eb7-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2eb7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2eb7-107">DESCRIPTION</span></span>
<span data-ttu-id="d2eb7-108">**New-AzDataFactoryDataset** cmdlet 'ı Azure Veri Fabrikası 'nde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="d2eb7-109">Zaten varolan bir veri kümesi için bir ad belirtirseniz, bu cmdlet veri kümesini değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="d2eb7-110">*Force* parametresini belirtirseniz, cmdlet var olan veri kümesini onay olmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="d2eb7-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="d2eb7-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="d2eb7-112">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-112">Create a data factory.</span></span> 
- <span data-ttu-id="d2eb7-113">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-113">Create linked services.</span></span> 
- <span data-ttu-id="d2eb7-114">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-114">Create datasets.</span></span> 
- <span data-ttu-id="d2eb7-115">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-115">Create a pipeline.</span></span>
<span data-ttu-id="d2eb7-116">Veri Fabrikası içinde aynı ada sahip bir veri kümesi varsa, bu cmdlet, var olan veri kümesinin yeni DataSet ile üzerine yazılmasını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="d2eb7-117">Var olan veri kümesinin üzerine yazmayı onayladıktan sonra, veri kümesi tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="d2eb7-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2eb7-118">EXAMPLES</span></span>

### <span data-ttu-id="d2eb7-119">Örnek 1: veri kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d2eb7-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="d2eb7-120">Bu komut WikiADF adındaki DA_WikipediaClickEvents adlı veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="d2eb7-121">Komut, veri kümesini DAWikipediaClickEvents.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="d2eb7-122">Örnek 2: yeni bir veri kümesinin uygunluk durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d2eb7-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="d2eb7-123">İlk komut, önceki örnekte olduğu gibi DA_WikipediaClickEvents adlı bir veri kümesi oluşturur ve bu veri kümesini $Dataset değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="d2eb7-124">İkinci komut, veri kümesinin uygunluk özelliği hakkında ayrıntıları görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="d2eb7-125">Örnek 3: yeni veri kümesinin konumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d2eb7-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="d2eb7-126">İlk komut, önceki örnekte olduğu gibi DA_WikipediaClickEvents adlı bir veri kümesi oluşturur ve bu veri kümesini $Dataset değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="d2eb7-127">İkinci komut, DataSet 'in location özelliğinin ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="d2eb7-128">Örnek 4: yeni bir veri kümesi için geçerlilik kurallarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d2eb7-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="d2eb7-129">İlk komut, önceki örnekte olduğu gibi DA_WikipediaClickEvents adlı bir veri kümesi oluşturur ve bu veri kümesini $Dataset değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="d2eb7-130">İkinci komut, DataSet 'in doğrulama kuralları hakkında ayrıntılı bilgi alır ve bunları ardışık düzen işlecini kullanarak Format-List cmdlet 'ine iletir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d2eb7-131">Bu Windows PowerShell cmdlet 'i sonuçları biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="d2eb7-132">Daha fazla bilgi için yazın `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="d2eb7-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="d2eb7-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2eb7-133">PARAMETERS</span></span>

### <span data-ttu-id="d2eb7-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d2eb7-134">-DataFactory</span></span>
<span data-ttu-id="d2eb7-135">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d2eb7-136">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2eb7-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d2eb7-137">-DataFactoryName</span></span>
<span data-ttu-id="d2eb7-138">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d2eb7-139">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2eb7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2eb7-140">-DefaultProfile</span></span>
<span data-ttu-id="d2eb7-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d2eb7-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2eb7-142">-Dosya</span><span class="sxs-lookup"><span data-stu-id="d2eb7-142">-File</span></span>
<span data-ttu-id="d2eb7-143">Veri kümesinin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2eb7-144">-Force</span><span class="sxs-lookup"><span data-stu-id="d2eb7-144">-Force</span></span>
<span data-ttu-id="d2eb7-145">Bu cmdlet 'in varolan bir veri kümesini, sizden onay istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d2eb7-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2eb7-146">-Name</span></span>
<span data-ttu-id="d2eb7-147">Oluşturulacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-147">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2eb7-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2eb7-148">-ResourceGroupName</span></span>
<span data-ttu-id="d2eb7-149">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d2eb7-150">Bu cmdlet, bu parametrenin belirttiği grupta bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2eb7-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2eb7-151">-Confirm</span></span>
<span data-ttu-id="d2eb7-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2eb7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2eb7-153">-WhatIf</span></span>
<span data-ttu-id="d2eb7-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2eb7-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2eb7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2eb7-156">CommonParameters</span></span>
<span data-ttu-id="d2eb7-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2eb7-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2eb7-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2eb7-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2eb7-159">INPUTS</span></span>

### <span data-ttu-id="d2eb7-160">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="d2eb7-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d2eb7-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d2eb7-161">System.String</span></span>

## <span data-ttu-id="d2eb7-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2eb7-162">OUTPUTS</span></span>

### <span data-ttu-id="d2eb7-163">Microsoft.Azure.Commands.DataFactories.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="d2eb7-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="d2eb7-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2eb7-164">NOTES</span></span>
* <span data-ttu-id="d2eb7-165">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="d2eb7-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d2eb7-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2eb7-166">RELATED LINKS</span></span>

[<span data-ttu-id="d2eb7-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d2eb7-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="d2eb7-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d2eb7-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


