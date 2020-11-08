---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938280"
---
# <span data-ttu-id="f8fac-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8fac-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f8fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8fac-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fac-103">Veri Fabrikası içinde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8fac-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="f8fac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8fac-104">SYNTAX</span></span>

### <span data-ttu-id="f8fac-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8fac-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8fac-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f8fac-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8fac-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8fac-107">DESCRIPTION</span></span>
<span data-ttu-id="f8fac-108">Set-AzDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'nde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8fac-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="f8fac-109">Önceden var olan bir ardışık düzen için ad belirtirseniz, cmdlet, ardışık düzeni değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="f8fac-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="f8fac-110">Force parametresini belirtirseniz, cmdlet mevcut ardışık düzenin yerine geçer.</span><span class="sxs-lookup"><span data-stu-id="f8fac-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="f8fac-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:--Veri Fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f8fac-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="f8fac-112">--Bağlantılı hizmetler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f8fac-112">-- Create linked services.</span></span>
<span data-ttu-id="f8fac-113">--Veri kümeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f8fac-113">-- Create datasets.</span></span>
<span data-ttu-id="f8fac-114">--Ardışık düzen oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f8fac-114">-- Create a pipeline.</span></span>
<span data-ttu-id="f8fac-115">Veri Fabrikası içinde aynı ada sahip bir ardışık düzen varsa, bu cmdlet yeni ardışık düzenin mevcut ardışık düzenin üzerine yazılıp yazılmayacağını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8fac-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="f8fac-116">Mevcut ardışık düzenin üzerine yazılmasını onaylamıyorsanız, ardışık düzen tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="f8fac-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="f8fac-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8fac-117">EXAMPLES</span></span>

### <span data-ttu-id="f8fac-118">Örnek 1: ardışık düzen oluşturma</span><span class="sxs-lookup"><span data-stu-id="f8fac-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="f8fac-119">Bu komut, ADF adlı veri fabrikası içinde Dpwiöörnek adlı bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8fac-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="f8fac-120">Komut, ardışık düzeni DPWikisample.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="f8fac-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="f8fac-121">Bu dosya, ardışık düzene kopyalama etkinliği ve HDInsight etkinliği gibi etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="f8fac-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="f8fac-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8fac-122">PARAMETERS</span></span>

### <span data-ttu-id="f8fac-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f8fac-123">-DataFactoryName</span></span>
<span data-ttu-id="f8fac-124">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8fac-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f8fac-125">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8fac-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8fac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fac-126">-DefaultProfile</span></span>
<span data-ttu-id="f8fac-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8fac-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8fac-128">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="f8fac-128">-DefinitionFile</span></span>
<span data-ttu-id="f8fac-129">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="f8fac-129">The JSON file path.</span></span>

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

### <span data-ttu-id="f8fac-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f8fac-130">-Force</span></span>
<span data-ttu-id="f8fac-131">Bu cmdlet 'in mevcut bir ardışık düzeni sizden onay istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8fac-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f8fac-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8fac-132">-Name</span></span>
<span data-ttu-id="f8fac-133">Oluşturulacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8fac-133">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8fac-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fac-134">-ResourceGroupName</span></span>
<span data-ttu-id="f8fac-135">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8fac-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f8fac-136">Bu cmdlet, bu parametrenin belirttiği grup için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8fac-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8fac-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f8fac-137">-ResourceId</span></span>
<span data-ttu-id="f8fac-138">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f8fac-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f8fac-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8fac-139">-Confirm</span></span>
<span data-ttu-id="f8fac-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8fac-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8fac-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8fac-141">-WhatIf</span></span>
<span data-ttu-id="f8fac-142">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="f8fac-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f8fac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fac-143">CommonParameters</span></span>
<span data-ttu-id="f8fac-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8fac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fac-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8fac-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fac-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8fac-146">INPUTS</span></span>

### <span data-ttu-id="f8fac-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f8fac-147">System.String</span></span>

## <span data-ttu-id="f8fac-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8fac-148">OUTPUTS</span></span>

### <span data-ttu-id="f8fac-149">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f8fac-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="f8fac-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8fac-150">NOTES</span></span>
<span data-ttu-id="f8fac-151">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="f8fac-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f8fac-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8fac-152">RELATED LINKS</span></span>

[<span data-ttu-id="f8fac-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8fac-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f8fac-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8fac-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f8fac-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f8fac-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()