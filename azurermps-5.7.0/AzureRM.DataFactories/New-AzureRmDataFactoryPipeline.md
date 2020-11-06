---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dbdefb2e6fa419898447c17053f58631b35a906d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591015"
---
# <span data-ttu-id="be536-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="be536-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="be536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be536-102">SYNOPSIS</span></span>
<span data-ttu-id="be536-103">Veri Fabrikası içinde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be536-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be536-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be536-104">SYNTAX</span></span>

### <span data-ttu-id="be536-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be536-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be536-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="be536-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be536-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="be536-107">DESCRIPTION</span></span>
<span data-ttu-id="be536-108">**Yeni-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'nde bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be536-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="be536-109">Önceden var olan bir ardışık düzen için ad belirtirseniz, cmdlet, ardışık düzeni değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="be536-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="be536-110">*Force* parametresini belirtirseniz, cmdlet mevcut ardışık düzenin yerine geçer.</span><span class="sxs-lookup"><span data-stu-id="be536-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="be536-111">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="be536-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="be536-112">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="be536-112">Create a data factory.</span></span> 
- <span data-ttu-id="be536-113">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="be536-113">Create linked services.</span></span> 
- <span data-ttu-id="be536-114">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="be536-114">Create datasets.</span></span> 
- <span data-ttu-id="be536-115">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="be536-115">Create a pipeline.</span></span>

<span data-ttu-id="be536-116">Veri Fabrikası içinde aynı ada sahip bir ardışık düzen varsa, bu cmdlet yeni ardışık düzenin mevcut ardışık düzenin üzerine yazılıp yazılmayacağını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be536-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="be536-117">Mevcut ardışık düzenin üzerine yazılmasını onaylamıyorsanız, ardışık düzen tanımı da değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="be536-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="be536-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be536-118">EXAMPLES</span></span>

### <span data-ttu-id="be536-119">Örnek 1: ardışık düzen oluşturma</span><span class="sxs-lookup"><span data-stu-id="be536-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="be536-120">Bu komut, ADF adlı veri fabrikası içinde Dpwiöörnek adlı bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be536-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="be536-121">Komut, ardışık düzeni DPWikisample.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="be536-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="be536-122">Bu dosya, ardışık düzene kopyalama etkinliği ve HDInsight etkinliği gibi etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="be536-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="be536-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be536-123">PARAMETERS</span></span>

### <span data-ttu-id="be536-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="be536-124">-DataFactory</span></span>
<span data-ttu-id="be536-125">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be536-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="be536-126">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be536-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be536-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="be536-127">-DataFactoryName</span></span>
<span data-ttu-id="be536-128">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be536-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="be536-129">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be536-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="be536-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be536-130">-DefaultProfile</span></span>
<span data-ttu-id="be536-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="be536-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be536-132">-Dosya</span><span class="sxs-lookup"><span data-stu-id="be536-132">-File</span></span>
<span data-ttu-id="be536-133">Ardışık düzenin açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be536-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be536-134">-Force</span><span class="sxs-lookup"><span data-stu-id="be536-134">-Force</span></span>
<span data-ttu-id="be536-135">Bu cmdlet 'in mevcut bir ardışık düzeni sizden onay istemeden değiştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="be536-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="be536-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="be536-136">-Name</span></span>
<span data-ttu-id="be536-137">Oluşturulacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be536-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be536-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be536-138">-ResourceGroupName</span></span>
<span data-ttu-id="be536-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be536-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="be536-140">Bu cmdlet, bu parametrenin belirttiği grup için bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be536-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="be536-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="be536-141">-Confirm</span></span>
<span data-ttu-id="be536-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be536-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be536-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be536-143">-WhatIf</span></span>
<span data-ttu-id="be536-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be536-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be536-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be536-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be536-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be536-146">CommonParameters</span></span>
<span data-ttu-id="be536-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be536-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be536-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be536-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be536-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be536-149">INPUTS</span></span>

### <span data-ttu-id="be536-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="be536-150">None</span></span>
<span data-ttu-id="be536-151">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="be536-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be536-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be536-152">OUTPUTS</span></span>

### <span data-ttu-id="be536-153">Microsoft. Windowsazme. Commands. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="be536-153">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="be536-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be536-154">NOTES</span></span>
* <span data-ttu-id="be536-155">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="be536-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="be536-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be536-156">RELATED LINKS</span></span>

[<span data-ttu-id="be536-157">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="be536-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="be536-158">Remove-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="be536-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="be536-159">Özgeçmiş-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="be536-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="be536-160">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="be536-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="be536-161">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="be536-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


