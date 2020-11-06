---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 7ddbc2809c58172eea2cd98ce048e0e49fbb14f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589841"
---
# <span data-ttu-id="359e0-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="359e0-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="359e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="359e0-102">SYNOPSIS</span></span>
<span data-ttu-id="359e0-103">Bir veri fabrikası içinde bir PITe çalışmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="359e0-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="359e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="359e0-104">SYNTAX</span></span>

### <span data-ttu-id="359e0-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="359e0-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="359e0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="359e0-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="359e0-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="359e0-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="359e0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="359e0-108">DESCRIPTION</span></span>
<span data-ttu-id="359e0-109">**Stop-AzureRmDataFactoryV2PipelineRun** cmdlet 'i, PIELINE Run kimliğiyle belirtilen veri fabrikasında bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="359e0-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="359e0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="359e0-110">EXAMPLES</span></span>

### <span data-ttu-id="359e0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="359e0-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="359e0-112">Bu komut, fabrika WikiADF 'de kimliği b9730a13-AA12-4926-a8b3-8e3a974ab0bd olan ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="359e0-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="359e0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="359e0-113">PARAMETERS</span></span>

### <span data-ttu-id="359e0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="359e0-114">-DataFactory</span></span>
<span data-ttu-id="359e0-115">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="359e0-115">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="359e0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="359e0-116">-DataFactoryName</span></span>
<span data-ttu-id="359e0-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="359e0-117">The data factory name.</span></span>

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

### <span data-ttu-id="359e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359e0-118">-DefaultProfile</span></span>
<span data-ttu-id="359e0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="359e0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="359e0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="359e0-120">-InputObject</span></span>
<span data-ttu-id="359e0-121">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="359e0-121">The Run ID of the pipeline.</span></span>

```yaml
Type: PSPipelineRun
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="359e0-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="359e0-122">-PassThru</span></span>
<span data-ttu-id="359e0-123">Belirtildiyse, Case 'in cmdlet 'i doğru yazma işlemi başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="359e0-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="359e0-124">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="359e0-124">-PipelineRunId</span></span>
<span data-ttu-id="359e0-125">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="359e0-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="359e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="359e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="359e0-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="359e0-127">The resource group name.</span></span>

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

### <span data-ttu-id="359e0-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="359e0-128">-Confirm</span></span>
<span data-ttu-id="359e0-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="359e0-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="359e0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="359e0-130">-WhatIf</span></span>
<span data-ttu-id="359e0-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="359e0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="359e0-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="359e0-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="359e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359e0-133">CommonParameters</span></span>
<span data-ttu-id="359e0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="359e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359e0-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="359e0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359e0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="359e0-136">INPUTS</span></span>

### <span data-ttu-id="359e0-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="359e0-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="359e0-138">System. String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="359e0-138">System.String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="359e0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="359e0-139">OUTPUTS</span></span>

### <span data-ttu-id="359e0-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="359e0-140">System.Boolean</span></span>

## <span data-ttu-id="359e0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="359e0-141">NOTES</span></span>

## <span data-ttu-id="359e0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="359e0-142">RELATED LINKS</span></span>

