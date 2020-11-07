---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 311073fcd840e9d163c1316019e48569f7e59c81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765189"
---
# <span data-ttu-id="ab616-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ab616-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="ab616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab616-102">SYNOPSIS</span></span>
<span data-ttu-id="ab616-103">Veri Fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab616-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab616-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab616-104">SYNTAX</span></span>

### <span data-ttu-id="ab616-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ab616-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ab616-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ab616-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ab616-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab616-107">DESCRIPTION</span></span>
<span data-ttu-id="ab616-108">Set-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'nde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab616-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="ab616-109">Zaten varolan bir veri kümesi için bir ad belirtirseniz, bu cmdlet veri kümesini değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab616-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="ab616-110">Force parametresini belirtirseniz, cmdlet var olan veri kümesini onay olmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ab616-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="ab616-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="ab616-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="ab616-112">Veri Fabrikası içinde aynı ada sahip bir veri kümesi varsa, bu cmdlet, var olan veri kümesinin yeni DataSet ile üzerine yazılmasını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab616-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="ab616-113">Var olan veri kümesinin üzerine yazmayı onayladıktan sonra, veri kümesi tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ab616-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="ab616-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab616-114">EXAMPLES</span></span>

### <span data-ttu-id="ab616-115">Örnek 1: veri kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ab616-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="ab616-116">Bu komut WikiADF adındaki DA_WikipediaClickEvents adlı veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab616-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="ab616-117">Komut, veri kümesini DAWikipediaClickEvents.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="ab616-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="ab616-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab616-118">PARAMETERS</span></span>

### <span data-ttu-id="ab616-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab616-119">-Confirm</span></span>
<span data-ttu-id="ab616-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab616-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab616-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ab616-121">-DataFactoryName</span></span>
<span data-ttu-id="ab616-122">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab616-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ab616-123">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab616-123">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ab616-124">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="ab616-124">-DefinitionFile</span></span>
<span data-ttu-id="ab616-125">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="ab616-125">The JSON file path.</span></span>

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

### <span data-ttu-id="ab616-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ab616-126">-Force</span></span>
<span data-ttu-id="ab616-127">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ab616-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ab616-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab616-128">-Name</span></span>
<span data-ttu-id="ab616-129">Oluşturulacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab616-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab616-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab616-130">-ResourceGroupName</span></span>
<span data-ttu-id="ab616-131">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab616-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ab616-132">Bu cmdlet, bu parametrenin belirttiği grupta bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab616-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ab616-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ab616-133">-ResourceId</span></span>
<span data-ttu-id="ab616-134">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ab616-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ab616-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab616-135">-WhatIf</span></span>
<span data-ttu-id="ab616-136">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="ab616-136">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="ab616-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab616-137">INPUTS</span></span>

### <span data-ttu-id="ab616-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ab616-138">System.String</span></span>


## <span data-ttu-id="ab616-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab616-139">OUTPUTS</span></span>

### <span data-ttu-id="ab616-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="ab616-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="ab616-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab616-141">NOTES</span></span>
<span data-ttu-id="ab616-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="ab616-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ab616-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab616-143">RELATED LINKS</span></span>
[<span data-ttu-id="ab616-144">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ab616-144">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="ab616-145">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ab616-145">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
