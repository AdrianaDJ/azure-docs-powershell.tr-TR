---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 405ec877f139865082d21eb2c05ace17f1100e2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586722"
---
# <span data-ttu-id="317c7-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="317c7-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="317c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="317c7-102">SYNOPSIS</span></span>
<span data-ttu-id="317c7-103">Veri Fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c7-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="317c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="317c7-104">SYNTAX</span></span>

### <span data-ttu-id="317c7-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="317c7-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="317c7-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="317c7-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="317c7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="317c7-107">DESCRIPTION</span></span>
<span data-ttu-id="317c7-108">Set-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'nde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c7-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="317c7-109">Zaten varolan bir veri kümesi için bir ad belirtirseniz, bu cmdlet veri kümesini değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="317c7-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="317c7-110">Force parametresini belirtirseniz, cmdlet var olan veri kümesini onay olmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="317c7-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="317c7-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="317c7-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="317c7-112">Veri Fabrikası içinde aynı ada sahip bir veri kümesi varsa, bu cmdlet, var olan veri kümesinin yeni DataSet ile üzerine yazılmasını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="317c7-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="317c7-113">Var olan veri kümesinin üzerine yazmayı onayladıktan sonra, veri kümesi tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="317c7-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="317c7-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="317c7-114">EXAMPLES</span></span>

### <span data-ttu-id="317c7-115">Örnek 1: veri kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="317c7-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="317c7-116">Bu komut WikiADF adındaki DA_WikipediaClickEvents adlı veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c7-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="317c7-117">Komut, veri kümesini DAWikipediaClickEvents.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="317c7-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="317c7-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="317c7-118">PARAMETERS</span></span>

### <span data-ttu-id="317c7-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="317c7-119">-DataFactoryName</span></span>
<span data-ttu-id="317c7-120">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c7-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="317c7-121">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c7-121">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="317c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317c7-122">-DefaultProfile</span></span>
<span data-ttu-id="317c7-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="317c7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="317c7-124">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="317c7-124">-DefinitionFile</span></span>
<span data-ttu-id="317c7-125">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="317c7-125">The JSON file path.</span></span>

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

### <span data-ttu-id="317c7-126">-Force</span><span class="sxs-lookup"><span data-stu-id="317c7-126">-Force</span></span>
<span data-ttu-id="317c7-127">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="317c7-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="317c7-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="317c7-128">-Name</span></span>
<span data-ttu-id="317c7-129">Oluşturulacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c7-129">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="317c7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317c7-130">-ResourceGroupName</span></span>
<span data-ttu-id="317c7-131">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c7-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="317c7-132">Bu cmdlet, bu parametrenin belirttiği grupta bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c7-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="317c7-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="317c7-133">-ResourceId</span></span>
<span data-ttu-id="317c7-134">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="317c7-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="317c7-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="317c7-135">-Confirm</span></span>
<span data-ttu-id="317c7-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="317c7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="317c7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="317c7-137">-WhatIf</span></span>
<span data-ttu-id="317c7-138">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="317c7-138">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="317c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317c7-139">CommonParameters</span></span>
<span data-ttu-id="317c7-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="317c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317c7-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317c7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317c7-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="317c7-142">INPUTS</span></span>

### <span data-ttu-id="317c7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="317c7-143">System.String</span></span>

## <span data-ttu-id="317c7-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="317c7-144">OUTPUTS</span></span>

### <span data-ttu-id="317c7-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="317c7-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="317c7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="317c7-146">NOTES</span></span>
<span data-ttu-id="317c7-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="317c7-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="317c7-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="317c7-148">RELATED LINKS</span></span>

[<span data-ttu-id="317c7-149">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="317c7-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="317c7-150">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="317c7-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
