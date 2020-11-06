---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 63bb7337e7473d27838b08763ebe2a7de14514a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587975"
---
# <span data-ttu-id="40119-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40119-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="40119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40119-102">SYNOPSIS</span></span>
<span data-ttu-id="40119-103">Veri Fabrikası 'nde askıya alınan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="40119-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40119-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40119-104">SYNTAX</span></span>

### <span data-ttu-id="40119-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40119-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40119-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="40119-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40119-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="40119-107">DESCRIPTION</span></span>
<span data-ttu-id="40119-108">**Özgeçmiş-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'nde askıya alınan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="40119-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="40119-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40119-109">EXAMPLES</span></span>

### <span data-ttu-id="40119-110">Örnek 1: ardışık düzeni sürdürme</span><span class="sxs-lookup"><span data-stu-id="40119-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="40119-111">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="40119-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="40119-112">Bir ardışık düzeni askıya almak için **Suspend-Azurermdatafactorypeeline** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="40119-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="40119-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="40119-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="40119-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40119-114">PARAMETERS</span></span>

### <span data-ttu-id="40119-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="40119-115">-DataFactory</span></span>
<span data-ttu-id="40119-116">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40119-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="40119-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="40119-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40119-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="40119-118">-DataFactoryName</span></span>
<span data-ttu-id="40119-119">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40119-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="40119-120">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="40119-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40119-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="40119-121">-Name</span></span>
<span data-ttu-id="40119-122">Devam etmek için ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40119-122">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="40119-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40119-123">-ResourceGroupName</span></span>
<span data-ttu-id="40119-124">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40119-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="40119-125">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ardışık düzeni sürdürür.</span><span class="sxs-lookup"><span data-stu-id="40119-125">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="40119-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="40119-126">-Confirm</span></span>
<span data-ttu-id="40119-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40119-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40119-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40119-128">-WhatIf</span></span>
<span data-ttu-id="40119-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40119-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40119-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40119-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40119-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40119-131">-DefaultProfile</span></span>
<span data-ttu-id="40119-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40119-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40119-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40119-133">CommonParameters</span></span>
<span data-ttu-id="40119-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40119-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40119-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40119-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40119-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40119-136">INPUTS</span></span>

## <span data-ttu-id="40119-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40119-137">OUTPUTS</span></span>

### <span data-ttu-id="40119-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40119-138">System.Boolean</span></span>

## <span data-ttu-id="40119-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40119-139">NOTES</span></span>
* <span data-ttu-id="40119-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="40119-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="40119-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40119-141">RELATED LINKS</span></span>

[<span data-ttu-id="40119-142">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="40119-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40119-143">Yeni-Azurermdatafactorypeline</span><span class="sxs-lookup"><span data-stu-id="40119-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40119-144">Remove-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="40119-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40119-145">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="40119-145">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="40119-146">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="40119-146">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


