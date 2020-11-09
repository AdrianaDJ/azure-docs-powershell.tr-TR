---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320973"
---
# <span data-ttu-id="d8bf2-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="d8bf2-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="d8bf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8bf2-102">SYNOPSIS</span></span>
 <span data-ttu-id="d8bf2-103">Tetik çalıştırmasının başka bir örneğini çağırır.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="d8bf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8bf2-104">SYNTAX</span></span>

### <span data-ttu-id="d8bf2-105">ByFactoryNameByParameterFile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8bf2-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8bf2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d8bf2-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8bf2-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8bf2-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8bf2-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d8bf2-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8bf2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8bf2-109">DESCRIPTION</span></span>
<span data-ttu-id="d8bf2-110">**Invoke-AzDataFactoryV2TriggerRun** komutu, yeni tetik Run kimliğiyle bir tetikleyicinin bir kopyasının çalıştırılmasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="d8bf2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8bf2-111">EXAMPLES</span></span>

### <span data-ttu-id="d8bf2-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8bf2-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="d8bf2-113">Yeni tetik çalıştırması kimliğiyle bir tetikleyicinin bir başka örneğini başlatır, orijinal tetik çalıştırıldığında aynı pencerede başlangıçsaati ve başlangıç saati 'ni saklayın.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="d8bf2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8bf2-114">PARAMETERS</span></span>

### <span data-ttu-id="d8bf2-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8bf2-115">-DataFactory</span></span>
<span data-ttu-id="d8bf2-116">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-116">The data factory object.</span></span>

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

### <span data-ttu-id="d8bf2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8bf2-117">-DataFactoryName</span></span>
<span data-ttu-id="d8bf2-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-118">The data factory name.</span></span>

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

### <span data-ttu-id="d8bf2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8bf2-119">-DefaultProfile</span></span>
<span data-ttu-id="d8bf2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8bf2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8bf2-121">-InputObject</span></span>
<span data-ttu-id="d8bf2-122">Tetik ile ilgili bilgiler.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="d8bf2-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d8bf2-123">-PassThru</span></span>
<span data-ttu-id="d8bf2-124">Belirtildiyse, Case 'in cmdlet 'i doğru yazma işlemi başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="d8bf2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8bf2-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8bf2-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-126">The resource group name.</span></span>

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

### <span data-ttu-id="d8bf2-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="d8bf2-127">-TriggerName</span></span>
<span data-ttu-id="d8bf2-128">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-128">The trigger name.</span></span>

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

### <span data-ttu-id="d8bf2-129">-Triggerrunıd</span><span class="sxs-lookup"><span data-stu-id="d8bf2-129">-TriggerRunId</span></span>
<span data-ttu-id="d8bf2-130">Tetikleyicinin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="d8bf2-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8bf2-131">-Confirm</span></span>
<span data-ttu-id="d8bf2-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8bf2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8bf2-133">-WhatIf</span></span>
<span data-ttu-id="d8bf2-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8bf2-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8bf2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8bf2-136">CommonParameters</span></span>
<span data-ttu-id="d8bf2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8bf2-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8bf2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8bf2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8bf2-139">INPUTS</span></span>

### <span data-ttu-id="d8bf2-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggerrun</span><span class="sxs-lookup"><span data-stu-id="d8bf2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="d8bf2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d8bf2-141">System.String</span></span>

### <span data-ttu-id="d8bf2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="d8bf2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d8bf2-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8bf2-143">OUTPUTS</span></span>

### <span data-ttu-id="d8bf2-144">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="d8bf2-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="d8bf2-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8bf2-145">NOTES</span></span>

## <span data-ttu-id="d8bf2-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8bf2-146">RELATED LINKS</span></span>
