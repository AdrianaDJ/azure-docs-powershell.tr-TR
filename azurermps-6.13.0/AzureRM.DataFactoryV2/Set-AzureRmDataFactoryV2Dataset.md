---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 46d631c9fed6906db44bc91b6f8624abb4499ddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590328"
---
# <span data-ttu-id="f5b57-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="f5b57-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="f5b57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5b57-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b57-103">Veri Fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5b57-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5b57-104">SYNTAX</span></span>

### <span data-ttu-id="f5b57-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5b57-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5b57-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f5b57-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5b57-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5b57-107">DESCRIPTION</span></span>
<span data-ttu-id="f5b57-108">Set-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'nde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5b57-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="f5b57-109">Zaten varolan bir veri kümesi için bir ad belirtirseniz, bu cmdlet veri kümesini değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5b57-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="f5b57-110">Force parametresini belirtirseniz, cmdlet var olan veri kümesini onay olmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f5b57-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="f5b57-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:--Veri Fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5b57-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="f5b57-112">--Bağlantılı hizmetler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5b57-112">-- Create linked services.</span></span>
<span data-ttu-id="f5b57-113">--Veri kümeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5b57-113">-- Create datasets.</span></span>
<span data-ttu-id="f5b57-114">--Ardışık düzen oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5b57-114">-- Create a pipeline.</span></span>
<span data-ttu-id="f5b57-115">Veri Fabrikası içinde aynı ada sahip bir veri kümesi varsa, bu cmdlet, var olan veri kümesinin yeni DataSet ile üzerine yazılmasını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5b57-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="f5b57-116">Var olan veri kümesinin üzerine yazmayı onayladıktan sonra, veri kümesi tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="f5b57-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="f5b57-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5b57-117">EXAMPLES</span></span>

### <span data-ttu-id="f5b57-118">Örnek 1: veri kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f5b57-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="f5b57-119">Bu komut WikiADF adındaki DA_WikipediaClickEvents adlı veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5b57-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="f5b57-120">Komut, veri kümesini DAWikipediaClickEvents.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="f5b57-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="f5b57-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5b57-121">PARAMETERS</span></span>

### <span data-ttu-id="f5b57-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f5b57-122">-DataFactoryName</span></span>
<span data-ttu-id="f5b57-123">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5b57-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f5b57-124">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5b57-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5b57-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b57-125">-DefaultProfile</span></span>
<span data-ttu-id="f5b57-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5b57-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b57-127">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="f5b57-127">-DefinitionFile</span></span>
<span data-ttu-id="f5b57-128">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="f5b57-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b57-129">-Force</span><span class="sxs-lookup"><span data-stu-id="f5b57-129">-Force</span></span>
<span data-ttu-id="f5b57-130">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="f5b57-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f5b57-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5b57-131">-Name</span></span>
<span data-ttu-id="f5b57-132">Oluşturulacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5b57-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5b57-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5b57-133">-ResourceGroupName</span></span>
<span data-ttu-id="f5b57-134">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5b57-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f5b57-135">Bu cmdlet, bu parametrenin belirttiği grupta bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5b57-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5b57-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f5b57-136">-ResourceId</span></span>
<span data-ttu-id="f5b57-137">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f5b57-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f5b57-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5b57-138">-Confirm</span></span>
<span data-ttu-id="f5b57-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5b57-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5b57-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5b57-140">-WhatIf</span></span>
<span data-ttu-id="f5b57-141">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="f5b57-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f5b57-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b57-142">CommonParameters</span></span>
<span data-ttu-id="f5b57-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5b57-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b57-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b57-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b57-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5b57-145">INPUTS</span></span>

### <span data-ttu-id="f5b57-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f5b57-146">System.String</span></span>

## <span data-ttu-id="f5b57-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5b57-147">OUTPUTS</span></span>

### <span data-ttu-id="f5b57-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="f5b57-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="f5b57-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5b57-149">NOTES</span></span>
<span data-ttu-id="f5b57-150">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="f5b57-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5b57-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5b57-151">RELATED LINKS</span></span>

[<span data-ttu-id="f5b57-152">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="f5b57-152">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="f5b57-153">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="f5b57-153">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
