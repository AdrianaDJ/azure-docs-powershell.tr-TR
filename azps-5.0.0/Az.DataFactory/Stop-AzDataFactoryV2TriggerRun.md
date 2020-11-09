---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320789"
---
# <span data-ttu-id="2db90-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="2db90-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="2db90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db90-102">SYNOPSIS</span></span>
<span data-ttu-id="2db90-103">Bir veri fabrikası içinde bir tetikleyiciyi çalıştırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="2db90-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="2db90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2db90-104">SYNTAX</span></span>

### <span data-ttu-id="2db90-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2db90-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db90-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2db90-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db90-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2db90-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2db90-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2db90-108">DESCRIPTION</span></span>
<span data-ttu-id="2db90-109">**Stop-AzDataFactoryV2TriggerRun** cmdlet 'i tetik Name ve tetık Run ID ile belirtilen bir veri fabrikasında çalıştırılan bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="2db90-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="2db90-110">Şu anda WaitingOnDependency durumundaki TumblingWindowTriggers için desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="2db90-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="2db90-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2db90-111">EXAMPLES</span></span>

### <span data-ttu-id="2db90-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2db90-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="2db90-113">Bu komut, fabrikanın fabrikada ' 08586002468005888497807248799CU16 ' ile çalıştırılmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2db90-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="2db90-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2db90-114">PARAMETERS</span></span>

### <span data-ttu-id="2db90-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2db90-115">-DataFactory</span></span>
<span data-ttu-id="2db90-116">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2db90-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2db90-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2db90-117">-DataFactoryName</span></span>
<span data-ttu-id="2db90-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="2db90-118">The data factory name.</span></span>

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

### <span data-ttu-id="2db90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db90-119">-DefaultProfile</span></span>
<span data-ttu-id="2db90-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2db90-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db90-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2db90-121">-InputObject</span></span>
<span data-ttu-id="2db90-122">Tetik ile ilgili bilgiler.</span><span class="sxs-lookup"><span data-stu-id="2db90-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2db90-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2db90-123">-PassThru</span></span>
<span data-ttu-id="2db90-124">Belirtildiyse, Case 'in cmdlet 'i doğru yazma işlemi başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="2db90-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="2db90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db90-125">-ResourceGroupName</span></span>
<span data-ttu-id="2db90-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2db90-126">The resource group name.</span></span>

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

### <span data-ttu-id="2db90-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="2db90-127">-TriggerName</span></span>
<span data-ttu-id="2db90-128">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="2db90-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db90-129">-Triggerrunıd</span><span class="sxs-lookup"><span data-stu-id="2db90-129">-TriggerRunId</span></span>
<span data-ttu-id="2db90-130">Tetikleyicinin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2db90-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db90-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="2db90-131">-Confirm</span></span>
<span data-ttu-id="2db90-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2db90-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db90-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db90-133">-WhatIf</span></span>
<span data-ttu-id="2db90-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2db90-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db90-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2db90-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db90-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db90-136">CommonParameters</span></span>
<span data-ttu-id="2db90-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2db90-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db90-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2db90-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db90-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2db90-139">INPUTS</span></span>

### <span data-ttu-id="2db90-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggerrun</span><span class="sxs-lookup"><span data-stu-id="2db90-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="2db90-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2db90-141">System.String</span></span>

### <span data-ttu-id="2db90-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="2db90-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2db90-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2db90-143">OUTPUTS</span></span>

### <span data-ttu-id="2db90-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2db90-144">System.Boolean</span></span>

## <span data-ttu-id="2db90-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2db90-145">NOTES</span></span>

## <span data-ttu-id="2db90-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2db90-146">RELATED LINKS</span></span>
