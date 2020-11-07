---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 221fb414464c062a2f1798223bfe68a09543d7c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761122"
---
# <span data-ttu-id="ba960-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ba960-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="ba960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba960-102">SYNOPSIS</span></span>
<span data-ttu-id="ba960-103">Veri Fabrikası 'nde askıya alınan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="ba960-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="ba960-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba960-104">SYNTAX</span></span>

### <span data-ttu-id="ba960-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba960-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba960-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ba960-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba960-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba960-107">DESCRIPTION</span></span>
<span data-ttu-id="ba960-108">**Özgeçmiş-Azveri Factorypipeline** cmdlet 'ı Azure Veri Fabrikası 'nde askıya alınan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="ba960-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="ba960-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba960-109">EXAMPLES</span></span>

### <span data-ttu-id="ba960-110">Örnek 1: ardışık düzeni sürdürme</span><span class="sxs-lookup"><span data-stu-id="ba960-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ba960-111">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="ba960-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="ba960-112">Bir ardışık düzeni askıya almak için **Suspend-Azdatafactoryptoreline** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba960-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="ba960-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba960-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="ba960-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba960-114">PARAMETERS</span></span>

### <span data-ttu-id="ba960-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba960-115">-DataFactory</span></span>
<span data-ttu-id="ba960-116">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba960-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ba960-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="ba960-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba960-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ba960-118">-DataFactoryName</span></span>
<span data-ttu-id="ba960-119">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba960-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ba960-120">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="ba960-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba960-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba960-121">-DefaultProfile</span></span>
<span data-ttu-id="ba960-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba960-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba960-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba960-123">-Name</span></span>
<span data-ttu-id="ba960-124">Devam etmek için ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba960-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="ba960-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba960-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba960-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba960-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ba960-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="ba960-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba960-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba960-128">-Confirm</span></span>
<span data-ttu-id="ba960-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba960-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba960-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba960-130">-WhatIf</span></span>
<span data-ttu-id="ba960-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba960-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba960-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba960-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba960-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba960-133">CommonParameters</span></span>
<span data-ttu-id="ba960-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba960-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba960-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba960-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba960-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba960-136">INPUTS</span></span>

### <span data-ttu-id="ba960-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ba960-137">System.String</span></span>

### <span data-ttu-id="ba960-138">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="ba960-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ba960-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba960-139">OUTPUTS</span></span>

### <span data-ttu-id="ba960-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba960-140">System.Boolean</span></span>

## <span data-ttu-id="ba960-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba960-141">NOTES</span></span>
* <span data-ttu-id="ba960-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="ba960-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ba960-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba960-143">RELATED LINKS</span></span>

[<span data-ttu-id="ba960-144">Get-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="ba960-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="ba960-145">Yeni-Azveri Factorypya</span><span class="sxs-lookup"><span data-stu-id="ba960-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="ba960-146">Remove-Azdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="ba960-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="ba960-147">Set-Azdatafactorypipelineactivedönem</span><span class="sxs-lookup"><span data-stu-id="ba960-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="ba960-148">Askıya al-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="ba960-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


