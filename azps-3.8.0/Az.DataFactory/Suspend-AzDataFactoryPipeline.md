---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938264"
---
# <span data-ttu-id="c0107-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="c0107-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="c0107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0107-102">SYNOPSIS</span></span>
<span data-ttu-id="c0107-103">Azure Veri Fabrikası 'nde bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="c0107-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="c0107-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0107-104">SYNTAX</span></span>

### <span data-ttu-id="c0107-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0107-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0107-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c0107-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0107-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0107-107">DESCRIPTION</span></span>
<span data-ttu-id="c0107-108">**Askıya al-AzDataFactoryPipeline** cmdlet, Azure Veri Fabrikası 'nde bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="c0107-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="c0107-109">Resume-AzDataFactoryPipeline cmdlet 'ini kullanarak ardışık düzene devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0107-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="c0107-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0107-110">EXAMPLES</span></span>

### <span data-ttu-id="c0107-111">Örnek 1: ardışık düzeni askıya alma</span><span class="sxs-lookup"><span data-stu-id="c0107-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="c0107-112">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="c0107-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="c0107-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0107-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="c0107-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0107-114">PARAMETERS</span></span>

### <span data-ttu-id="c0107-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c0107-115">-DataFactory</span></span>
<span data-ttu-id="c0107-116">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0107-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c0107-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="c0107-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0107-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c0107-118">-DataFactoryName</span></span>
<span data-ttu-id="c0107-119">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0107-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c0107-120">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="c0107-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0107-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0107-121">-DefaultProfile</span></span>
<span data-ttu-id="c0107-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c0107-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0107-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0107-123">-Name</span></span>
<span data-ttu-id="c0107-124">Askıya alınacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0107-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="c0107-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0107-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0107-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0107-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c0107-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ardışık düzeni askıya alır.</span><span class="sxs-lookup"><span data-stu-id="c0107-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0107-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0107-128">-Confirm</span></span>
<span data-ttu-id="c0107-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0107-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0107-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0107-130">-WhatIf</span></span>
<span data-ttu-id="c0107-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0107-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0107-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0107-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0107-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0107-133">CommonParameters</span></span>
<span data-ttu-id="c0107-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0107-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0107-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0107-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0107-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0107-136">INPUTS</span></span>

### <span data-ttu-id="c0107-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c0107-137">System.String</span></span>

### <span data-ttu-id="c0107-138">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="c0107-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c0107-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0107-139">OUTPUTS</span></span>

### <span data-ttu-id="c0107-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0107-140">System.Boolean</span></span>

## <span data-ttu-id="c0107-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0107-141">NOTES</span></span>
* <span data-ttu-id="c0107-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="c0107-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c0107-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0107-143">RELATED LINKS</span></span>

[<span data-ttu-id="c0107-144">Get-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="c0107-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="c0107-145">Yeni-Azveri Factorypya</span><span class="sxs-lookup"><span data-stu-id="c0107-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="c0107-146">Remove-Azdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="c0107-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="c0107-147">Özgeçmiş-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="c0107-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="c0107-148">Set-Azdatafactorypipelineactivedönem</span><span class="sxs-lookup"><span data-stu-id="c0107-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


