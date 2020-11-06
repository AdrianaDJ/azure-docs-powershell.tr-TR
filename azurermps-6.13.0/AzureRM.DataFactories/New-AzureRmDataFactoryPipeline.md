---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 7ad7eb0f87972c3a64b3fb966259d25d527c20c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588516"
---
# <span data-ttu-id="58a6f-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="58a6f-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="58a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="58a6f-103">Veri Fabrikası içinde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58a6f-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58a6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58a6f-104">SYNTAX</span></span>

### <span data-ttu-id="58a6f-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58a6f-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58a6f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="58a6f-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58a6f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="58a6f-107">DESCRIPTION</span></span>
<span data-ttu-id="58a6f-108">**Yeni-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'nde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58a6f-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="58a6f-109">Önceden var olan bir ardışık düzen için ad belirtirseniz, cmdlet, ardışık düzeni değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="58a6f-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="58a6f-110">*Force* parametresini belirtirseniz, cmdlet mevcut ardışık düzenin yerine geçer.</span><span class="sxs-lookup"><span data-stu-id="58a6f-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="58a6f-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="58a6f-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="58a6f-112">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="58a6f-112">Create a data factory.</span></span> 
- <span data-ttu-id="58a6f-113">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="58a6f-113">Create linked services.</span></span> 
- <span data-ttu-id="58a6f-114">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="58a6f-114">Create datasets.</span></span> 
- <span data-ttu-id="58a6f-115">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="58a6f-115">Create a pipeline.</span></span>
<span data-ttu-id="58a6f-116">Veri Fabrikası içinde aynı ada sahip bir ardışık düzen varsa, bu cmdlet yeni ardışık düzenin mevcut ardışık düzenin üzerine yazılıp yazılmayacağını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58a6f-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="58a6f-117">Mevcut ardışık düzenin üzerine yazılmasını onaylamıyorsanız, ardışık düzen tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="58a6f-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58a6f-118">EXAMPLES</span></span>

### <span data-ttu-id="58a6f-119">Örnek 1: ardışık düzen oluşturma</span><span class="sxs-lookup"><span data-stu-id="58a6f-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="58a6f-120">Bu komut, ADF adlı veri fabrikası içinde Dpwiöörnek adlı bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58a6f-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="58a6f-121">Komut, ardışık düzeni DPWikisample.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="58a6f-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="58a6f-122">Bu dosya, ardışık düzene kopyalama etkinliği ve HDInsight etkinliği gibi etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="58a6f-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58a6f-123">PARAMETERS</span></span>

### <span data-ttu-id="58a6f-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="58a6f-124">-DataFactory</span></span>
<span data-ttu-id="58a6f-125">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="58a6f-126">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58a6f-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="58a6f-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58a6f-127">-DataFactoryName</span></span>
<span data-ttu-id="58a6f-128">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="58a6f-129">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58a6f-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="58a6f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a6f-130">-DefaultProfile</span></span>
<span data-ttu-id="58a6f-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="58a6f-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58a6f-132">-Dosya</span><span class="sxs-lookup"><span data-stu-id="58a6f-132">-File</span></span>
<span data-ttu-id="58a6f-133">Ardışık düzenin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="58a6f-134">-Force</span><span class="sxs-lookup"><span data-stu-id="58a6f-134">-Force</span></span>
<span data-ttu-id="58a6f-135">Bu cmdlet 'in mevcut bir ardışık düzeni sizden onay istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="58a6f-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="58a6f-136">-Name</span></span>
<span data-ttu-id="58a6f-137">Oluşturulacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="58a6f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a6f-138">-ResourceGroupName</span></span>
<span data-ttu-id="58a6f-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="58a6f-140">Bu cmdlet, bu parametrenin belirttiği grup için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58a6f-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="58a6f-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="58a6f-141">-Confirm</span></span>
<span data-ttu-id="58a6f-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58a6f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a6f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a6f-143">-WhatIf</span></span>
<span data-ttu-id="58a6f-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58a6f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a6f-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58a6f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a6f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a6f-146">CommonParameters</span></span>
<span data-ttu-id="58a6f-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58a6f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a6f-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a6f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a6f-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58a6f-149">INPUTS</span></span>

### <span data-ttu-id="58a6f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="58a6f-150">System.String</span></span>

### <span data-ttu-id="58a6f-151">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="58a6f-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="58a6f-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58a6f-152">OUTPUTS</span></span>

### <span data-ttu-id="58a6f-153">Microsoft. Azure. Commands. DataFactory. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="58a6f-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="58a6f-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58a6f-154">NOTES</span></span>
* <span data-ttu-id="58a6f-155">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="58a6f-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="58a6f-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58a6f-156">RELATED LINKS</span></span>

[<span data-ttu-id="58a6f-157">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="58a6f-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="58a6f-158">Remove-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="58a6f-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="58a6f-159">Özgeçmiş-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="58a6f-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="58a6f-160">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="58a6f-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="58a6f-161">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="58a6f-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


