---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ae640ffb0f595419bba57ff92d7789692af55d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587976"
---
# <span data-ttu-id="3de7c-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3de7c-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="3de7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3de7c-103">Veri Fabrikası içinde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3de7c-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3de7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3de7c-104">SYNTAX</span></span>

### <span data-ttu-id="3de7c-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3de7c-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3de7c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3de7c-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de7c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3de7c-107">DESCRIPTION</span></span>
<span data-ttu-id="3de7c-108">**Yeni-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'nde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3de7c-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="3de7c-109">Önceden var olan bir ardışık düzen için ad belirtirseniz, cmdlet, ardışık düzeni değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="3de7c-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="3de7c-110">*Force* parametresini belirtirseniz, cmdlet mevcut ardışık düzenin yerine geçer.</span><span class="sxs-lookup"><span data-stu-id="3de7c-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="3de7c-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="3de7c-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="3de7c-112">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="3de7c-112">Create a data factory.</span></span> 
- <span data-ttu-id="3de7c-113">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="3de7c-113">Create linked services.</span></span> 
- <span data-ttu-id="3de7c-114">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="3de7c-114">Create datasets.</span></span> 
- <span data-ttu-id="3de7c-115">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="3de7c-115">Create a pipeline.</span></span>

<span data-ttu-id="3de7c-116">Veri Fabrikası içinde aynı ada sahip bir ardışık düzen varsa, bu cmdlet yeni ardışık düzenin mevcut ardışık düzenin üzerine yazılıp yazılmayacağını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3de7c-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="3de7c-117">Mevcut ardışık düzenin üzerine yazılmasını onaylamıyorsanız, ardışık düzen tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="3de7c-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3de7c-118">EXAMPLES</span></span>

### <span data-ttu-id="3de7c-119">Örnek 1: ardışık düzen oluşturma</span><span class="sxs-lookup"><span data-stu-id="3de7c-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="3de7c-120">Bu komut, ADF adlı veri fabrikası içinde Dpwiöörnek adlı bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3de7c-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="3de7c-121">Komut, ardışık düzeni DPWikisample.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="3de7c-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="3de7c-122">Bu dosya, ardışık düzene kopyalama etkinliği ve HDInsight etkinliği gibi etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="3de7c-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3de7c-123">PARAMETERS</span></span>

### <span data-ttu-id="3de7c-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3de7c-124">-DataFactory</span></span>
<span data-ttu-id="3de7c-125">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3de7c-126">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3de7c-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3de7c-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3de7c-127">-DataFactoryName</span></span>
<span data-ttu-id="3de7c-128">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3de7c-129">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3de7c-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3de7c-130">-Dosya</span><span class="sxs-lookup"><span data-stu-id="3de7c-130">-File</span></span>
<span data-ttu-id="3de7c-131">Ardışık düzenin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-131">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="3de7c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="3de7c-132">-Force</span></span>
<span data-ttu-id="3de7c-133">Bu cmdlet 'in mevcut bir ardışık düzeni sizden onay istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-133">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3de7c-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="3de7c-134">-Name</span></span>
<span data-ttu-id="3de7c-135">Oluşturulacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-135">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="3de7c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de7c-136">-ResourceGroupName</span></span>
<span data-ttu-id="3de7c-137">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3de7c-138">Bu cmdlet, bu parametrenin belirttiği grup için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3de7c-138">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3de7c-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="3de7c-139">-Confirm</span></span>
<span data-ttu-id="3de7c-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3de7c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de7c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de7c-141">-WhatIf</span></span>
<span data-ttu-id="3de7c-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3de7c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de7c-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3de7c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de7c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de7c-144">-DefaultProfile</span></span>
<span data-ttu-id="3de7c-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3de7c-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3de7c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de7c-146">CommonParameters</span></span>
<span data-ttu-id="3de7c-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3de7c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de7c-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de7c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de7c-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3de7c-149">INPUTS</span></span>

## <span data-ttu-id="3de7c-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3de7c-150">OUTPUTS</span></span>

### <span data-ttu-id="3de7c-151">Microsoft. Windowsazme. Commands. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="3de7c-151">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="3de7c-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3de7c-152">NOTES</span></span>
* <span data-ttu-id="3de7c-153">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="3de7c-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3de7c-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3de7c-154">RELATED LINKS</span></span>

[<span data-ttu-id="3de7c-155">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="3de7c-155">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="3de7c-156">Remove-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="3de7c-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="3de7c-157">Özgeçmiş-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="3de7c-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="3de7c-158">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="3de7c-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="3de7c-159">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="3de7c-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


