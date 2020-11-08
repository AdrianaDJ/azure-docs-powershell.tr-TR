---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095948"
---
# <span data-ttu-id="57ac4-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="57ac4-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="57ac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="57ac4-103">Veri Fabrikası 'ndan veri akışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57ac4-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="57ac4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57ac4-104">SYNTAX</span></span>

### <span data-ttu-id="57ac4-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57ac4-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57ac4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="57ac4-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57ac4-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="57ac4-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57ac4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="57ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="57ac4-109">Remove-AzDataFactoryV2DataFlow cmdlet 'i Azure Veri Fabrikası 'ndan veri akışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57ac4-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="57ac4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57ac4-110">EXAMPLES</span></span>

### <span data-ttu-id="57ac4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="57ac4-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="57ac4-112">Bu komut, WikiADF adındaki dataflow5 adındaki veri akışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57ac4-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="57ac4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57ac4-113">PARAMETERS</span></span>

### <span data-ttu-id="57ac4-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="57ac4-114">-DataFactoryName</span></span>
<span data-ttu-id="57ac4-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="57ac4-115">The data factory name.</span></span>

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

### <span data-ttu-id="57ac4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ac4-116">-DefaultProfile</span></span>
<span data-ttu-id="57ac4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57ac4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ac4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="57ac4-118">-Force</span></span>
<span data-ttu-id="57ac4-119">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="57ac4-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="57ac4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57ac4-120">-InputObject</span></span>
<span data-ttu-id="57ac4-121">Veri akışı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="57ac4-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57ac4-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="57ac4-122">-Name</span></span>
<span data-ttu-id="57ac4-123">Veri akışı adı.</span><span class="sxs-lookup"><span data-stu-id="57ac4-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ac4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ac4-124">-ResourceGroupName</span></span>
<span data-ttu-id="57ac4-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="57ac4-125">The resource group name.</span></span>

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

### <span data-ttu-id="57ac4-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="57ac4-126">-ResourceId</span></span>
<span data-ttu-id="57ac4-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="57ac4-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="57ac4-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="57ac4-128">-PassThru</span></span>
<span data-ttu-id="57ac4-129">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="57ac4-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="57ac4-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="57ac4-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="57ac4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="57ac4-131">-Confirm</span></span>
<span data-ttu-id="57ac4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57ac4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ac4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ac4-133">-WhatIf</span></span>
<span data-ttu-id="57ac4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57ac4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ac4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57ac4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ac4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ac4-136">CommonParameters</span></span>
<span data-ttu-id="57ac4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57ac4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ac4-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="57ac4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ac4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57ac4-139">INPUTS</span></span>

### <span data-ttu-id="57ac4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="57ac4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="57ac4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="57ac4-141">System.String</span></span>

## <span data-ttu-id="57ac4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57ac4-142">OUTPUTS</span></span>

### <span data-ttu-id="57ac4-143">System. void</span><span class="sxs-lookup"><span data-stu-id="57ac4-143">System.Void</span></span>

### <span data-ttu-id="57ac4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57ac4-144">System.Boolean</span></span>

## <span data-ttu-id="57ac4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57ac4-145">NOTES</span></span>
<span data-ttu-id="57ac4-146">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="57ac4-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="57ac4-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57ac4-147">RELATED LINKS</span></span>

[<span data-ttu-id="57ac4-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="57ac4-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="57ac4-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="57ac4-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

