---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938300"
---
# <span data-ttu-id="0f7d0-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="0f7d0-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="0f7d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7d0-103">Veri Fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="0f7d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f7d0-104">SYNTAX</span></span>

### <span data-ttu-id="0f7d0-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f7d0-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f7d0-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0f7d0-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f7d0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f7d0-107">DESCRIPTION</span></span>
<span data-ttu-id="0f7d0-108">Set-AzDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'nde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="0f7d0-109">Zaten varolan bir veri kümesi için bir ad belirtirseniz, bu cmdlet veri kümesini değiştirmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="0f7d0-110">Force parametresini belirtirseniz, cmdlet var olan veri kümesini onay olmadan değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="0f7d0-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:--Veri Fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="0f7d0-112">--Bağlantılı hizmetler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-112">-- Create linked services.</span></span>
<span data-ttu-id="0f7d0-113">--Veri kümeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-113">-- Create datasets.</span></span>
<span data-ttu-id="0f7d0-114">--Ardışık düzen oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-114">-- Create a pipeline.</span></span>
<span data-ttu-id="0f7d0-115">Veri Fabrikası içinde aynı ada sahip bir veri kümesi varsa, bu cmdlet, var olan veri kümesinin yeni DataSet ile üzerine yazılmasını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="0f7d0-116">Var olan veri kümesinin üzerine yazmayı onayladıktan sonra, veri kümesi tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="0f7d0-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f7d0-117">EXAMPLES</span></span>

### <span data-ttu-id="0f7d0-118">Örnek 1: veri kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0f7d0-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="0f7d0-119">Bu komut WikiADF adındaki DA_WikipediaClickEvents adlı veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="0f7d0-120">Komut, veri kümesini DAWikipediaClickEvents.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="0f7d0-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f7d0-121">PARAMETERS</span></span>

### <span data-ttu-id="0f7d0-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f7d0-122">-DataFactoryName</span></span>
<span data-ttu-id="0f7d0-123">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0f7d0-124">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içinde bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f7d0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7d0-125">-DefaultProfile</span></span>
<span data-ttu-id="0f7d0-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f7d0-127">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="0f7d0-127">-DefinitionFile</span></span>
<span data-ttu-id="0f7d0-128">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-128">The JSON file path.</span></span>

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

### <span data-ttu-id="0f7d0-129">-Force</span><span class="sxs-lookup"><span data-stu-id="0f7d0-129">-Force</span></span>
<span data-ttu-id="0f7d0-130">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0f7d0-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f7d0-131">-Name</span></span>
<span data-ttu-id="0f7d0-132">Oluşturulacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="0f7d0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f7d0-133">-ResourceGroupName</span></span>
<span data-ttu-id="0f7d0-134">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0f7d0-135">Bu cmdlet, bu parametrenin belirttiği grupta bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f7d0-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0f7d0-136">-ResourceId</span></span>
<span data-ttu-id="0f7d0-137">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0f7d0-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f7d0-138">-Confirm</span></span>
<span data-ttu-id="0f7d0-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f7d0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f7d0-140">-WhatIf</span></span>
<span data-ttu-id="0f7d0-141">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0f7d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7d0-142">CommonParameters</span></span>
<span data-ttu-id="0f7d0-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f7d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7d0-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f7d0-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7d0-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f7d0-145">INPUTS</span></span>

### <span data-ttu-id="0f7d0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0f7d0-146">System.String</span></span>

## <span data-ttu-id="0f7d0-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f7d0-147">OUTPUTS</span></span>

### <span data-ttu-id="0f7d0-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="0f7d0-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="0f7d0-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f7d0-149">NOTES</span></span>
<span data-ttu-id="0f7d0-150">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="0f7d0-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0f7d0-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f7d0-151">RELATED LINKS</span></span>

[<span data-ttu-id="0f7d0-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="0f7d0-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="0f7d0-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="0f7d0-153">Remove-AzDataFactoryV2Dataset</span></span>]()
