---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ecbf1a97ebaa7f4d008b63f9b7d4c49c49a09956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593685"
---
# <span data-ttu-id="059b4-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="059b4-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="059b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059b4-102">SYNOPSIS</span></span>
<span data-ttu-id="059b4-103">Azure Veri Fabrikası 'nde bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="059b4-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="059b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="059b4-104">SYNTAX</span></span>

### <span data-ttu-id="059b4-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="059b4-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059b4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="059b4-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="059b4-107">DESCRIPTION</span></span>
<span data-ttu-id="059b4-108">**Suspend-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'nde bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="059b4-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="059b4-109">Resume-AzureRmDataFactoryPipeline cmdlet 'ini kullanarak ardışık düzene devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="059b4-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="059b4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="059b4-110">EXAMPLES</span></span>

### <span data-ttu-id="059b4-111">Örnek 1: ardışık düzeni askıya alma</span><span class="sxs-lookup"><span data-stu-id="059b4-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="059b4-112">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="059b4-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="059b4-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="059b4-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="059b4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="059b4-114">PARAMETERS</span></span>

### <span data-ttu-id="059b4-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="059b4-115">-DataFactory</span></span>
<span data-ttu-id="059b4-116">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="059b4-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="059b4-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="059b4-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="059b4-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="059b4-118">-DataFactoryName</span></span>
<span data-ttu-id="059b4-119">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="059b4-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="059b4-120">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="059b4-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="059b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059b4-121">-DefaultProfile</span></span>
<span data-ttu-id="059b4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="059b4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="059b4-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="059b4-123">-Name</span></span>
<span data-ttu-id="059b4-124">Askıya alınacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="059b4-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059b4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059b4-125">-ResourceGroupName</span></span>
<span data-ttu-id="059b4-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="059b4-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="059b4-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="059b4-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="059b4-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="059b4-128">-Confirm</span></span>
<span data-ttu-id="059b4-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="059b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059b4-130">-WhatIf</span></span>
<span data-ttu-id="059b4-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="059b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="059b4-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="059b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059b4-133">CommonParameters</span></span>
<span data-ttu-id="059b4-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="059b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059b4-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059b4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059b4-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="059b4-136">INPUTS</span></span>

### <span data-ttu-id="059b4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="059b4-137">System.String</span></span>

### <span data-ttu-id="059b4-138">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="059b4-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="059b4-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="059b4-139">OUTPUTS</span></span>

### <span data-ttu-id="059b4-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="059b4-140">System.Boolean</span></span>

## <span data-ttu-id="059b4-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="059b4-141">NOTES</span></span>
* <span data-ttu-id="059b4-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="059b4-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="059b4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="059b4-143">RELATED LINKS</span></span>

[<span data-ttu-id="059b4-144">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="059b4-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="059b4-145">Yeni-Azurermdatafactorypeline</span><span class="sxs-lookup"><span data-stu-id="059b4-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="059b4-146">Remove-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="059b4-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="059b4-147">Özgeçmiş-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="059b4-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="059b4-148">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="059b4-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


