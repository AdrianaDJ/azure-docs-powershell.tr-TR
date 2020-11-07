---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: 6583da48324078d321630f23097ab3a00d8338d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761138"
---
# <span data-ttu-id="16739-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="16739-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="16739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16739-102">SYNOPSIS</span></span>
<span data-ttu-id="16739-103">Veri Fabrikası içinde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16739-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="16739-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16739-104">SYNTAX</span></span>

### <span data-ttu-id="16739-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16739-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16739-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="16739-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16739-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="16739-107">DESCRIPTION</span></span>
<span data-ttu-id="16739-108">**Yeni-Azverfactorypypeline** cmdlet, Azure Veri Fabrikası 'nde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16739-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="16739-109">Önceden var olan bir ardışık düzen için ad belirtirseniz, cmdlet, ardışık düzeni değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="16739-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="16739-110">*Force* parametresini belirtirseniz, cmdlet mevcut ardışık düzenin yerine geçer.</span><span class="sxs-lookup"><span data-stu-id="16739-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="16739-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="16739-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="16739-112">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="16739-112">Create a data factory.</span></span> 
- <span data-ttu-id="16739-113">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="16739-113">Create linked services.</span></span> 
- <span data-ttu-id="16739-114">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="16739-114">Create datasets.</span></span> 
- <span data-ttu-id="16739-115">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="16739-115">Create a pipeline.</span></span>
<span data-ttu-id="16739-116">Veri Fabrikası içinde aynı ada sahip bir ardışık düzen varsa, bu cmdlet yeni ardışık düzenin mevcut ardışık düzenin üzerine yazılıp yazılmayacağını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16739-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="16739-117">Mevcut ardışık düzenin üzerine yazılmasını onaylamıyorsanız, ardışık düzen tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="16739-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="16739-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16739-118">EXAMPLES</span></span>

### <span data-ttu-id="16739-119">Örnek 1: ardışık düzen oluşturma</span><span class="sxs-lookup"><span data-stu-id="16739-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="16739-120">Bu komut, ADF adlı veri fabrikası içinde Dpwiöörnek adlı bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16739-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="16739-121">Komut, ardışık düzeni DPWikisample.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="16739-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="16739-122">Bu dosya, ardışık düzene kopyalama etkinliği ve HDInsight etkinliği gibi etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="16739-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="16739-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16739-123">PARAMETERS</span></span>

### <span data-ttu-id="16739-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="16739-124">-DataFactory</span></span>
<span data-ttu-id="16739-125">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16739-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="16739-126">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16739-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="16739-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16739-127">-DataFactoryName</span></span>
<span data-ttu-id="16739-128">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16739-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="16739-129">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16739-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="16739-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16739-130">-DefaultProfile</span></span>
<span data-ttu-id="16739-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16739-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16739-132">-Dosya</span><span class="sxs-lookup"><span data-stu-id="16739-132">-File</span></span>
<span data-ttu-id="16739-133">Ardışık düzenin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="16739-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="16739-134">-Force</span><span class="sxs-lookup"><span data-stu-id="16739-134">-Force</span></span>
<span data-ttu-id="16739-135">Bu cmdlet 'in mevcut bir ardışık düzeni sizden onay istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="16739-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="16739-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="16739-136">-Name</span></span>
<span data-ttu-id="16739-137">Oluşturulacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16739-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="16739-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16739-138">-ResourceGroupName</span></span>
<span data-ttu-id="16739-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16739-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="16739-140">Bu cmdlet, bu parametrenin belirttiği grup için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16739-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16739-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="16739-141">-Confirm</span></span>
<span data-ttu-id="16739-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16739-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16739-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16739-143">-WhatIf</span></span>
<span data-ttu-id="16739-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16739-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16739-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16739-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16739-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16739-146">CommonParameters</span></span>
<span data-ttu-id="16739-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16739-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16739-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16739-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16739-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16739-149">INPUTS</span></span>

### <span data-ttu-id="16739-150">System. String</span><span class="sxs-lookup"><span data-stu-id="16739-150">System.String</span></span>

### <span data-ttu-id="16739-151">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="16739-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="16739-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16739-152">OUTPUTS</span></span>

### <span data-ttu-id="16739-153">Microsoft. Azure. Commands. DataFactory. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="16739-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="16739-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16739-154">NOTES</span></span>
* <span data-ttu-id="16739-155">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="16739-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="16739-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16739-156">RELATED LINKS</span></span>

[<span data-ttu-id="16739-157">Get-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="16739-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="16739-158">Remove-Azdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="16739-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="16739-159">Özgeçmiş-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="16739-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="16739-160">Set-Azdatafactorypipelineactivedönem</span><span class="sxs-lookup"><span data-stu-id="16739-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="16739-161">Askıya al-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="16739-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

