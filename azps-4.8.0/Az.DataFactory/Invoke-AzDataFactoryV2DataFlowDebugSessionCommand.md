---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275043"
---
# <span data-ttu-id="17268-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="17268-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="17268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17268-102">SYNOPSIS</span></span>
<span data-ttu-id="17268-103">Veri akışı hata ayıklama oturumunda hata ayıklama eylemini çağır.</span><span class="sxs-lookup"><span data-stu-id="17268-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="17268-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17268-104">SYNTAX</span></span>

### <span data-ttu-id="17268-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17268-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17268-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="17268-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17268-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="17268-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17268-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17268-108">DESCRIPTION</span></span>
<span data-ttu-id="17268-109">Bu komut, hata ayıklama oturumunda farklı veri akışı akışı için veri önizleme/istatistik önizleme/ifade önizlemeyi yürütür.</span><span class="sxs-lookup"><span data-stu-id="17268-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="17268-110">Veri akışı hata ayıklama iş akışı için PowerShell komut dizisi:</span><span class="sxs-lookup"><span data-stu-id="17268-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="17268-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="17268-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="17268-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="17268-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="17268-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (Bu adımı farklı komutlar/hedefler için tekrarlama veya paket dosyasını değiştirmek için 2-3 adımını tekrarlama)</span><span class="sxs-lookup"><span data-stu-id="17268-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="17268-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="17268-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="17268-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17268-115">EXAMPLES</span></span>

### <span data-ttu-id="17268-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="17268-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="17268-117">Bu örnekte, "WiKiADF" Veri Fabrikası "fd76cd0d-8b37-4dc0-A370-3f9d43ac686d" hata ayıklama oturumu</span><span class="sxs-lookup"><span data-stu-id="17268-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="17268-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17268-118">PARAMETERS</span></span>

### <span data-ttu-id="17268-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="17268-119">-AsJob</span></span>
<span data-ttu-id="17268-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="17268-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17268-121">-Sütunlar</span><span class="sxs-lookup"><span data-stu-id="17268-121">-Columns</span></span>
<span data-ttu-id="17268-122">Veri akışı istatistikleri önizlemesi için sütunlar listesi.</span><span class="sxs-lookup"><span data-stu-id="17268-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17268-123">-Komut</span><span class="sxs-lookup"><span data-stu-id="17268-123">-Command</span></span>
<span data-ttu-id="17268-124">Veri akışı hata ayıklaması komutu.</span><span class="sxs-lookup"><span data-stu-id="17268-124">The data flow debug command.</span></span> <span data-ttu-id="17268-125">Seçeneklerin, Executepreview sorgusu, executeStatisticsQuery ve executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="17268-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="17268-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="17268-126">-DataFactory</span></span>
<span data-ttu-id="17268-127">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="17268-127">The data factory object.</span></span>

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

### <span data-ttu-id="17268-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="17268-128">-DataFactoryName</span></span>
<span data-ttu-id="17268-129">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="17268-129">The data factory name.</span></span>

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

### <span data-ttu-id="17268-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17268-130">-DefaultProfile</span></span>
<span data-ttu-id="17268-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17268-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17268-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="17268-132">-Expression</span></span>
<span data-ttu-id="17268-133">Veri akışı ifade önizleme ifadesi.</span><span class="sxs-lookup"><span data-stu-id="17268-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17268-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17268-134">-ResourceGroupName</span></span>
<span data-ttu-id="17268-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="17268-135">The resource group name.</span></span>

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

### <span data-ttu-id="17268-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="17268-136">-ResourceId</span></span>
<span data-ttu-id="17268-137">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="17268-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="17268-138">-RowLimit</span><span class="sxs-lookup"><span data-stu-id="17268-138">-RowLimits</span></span>
<span data-ttu-id="17268-139">Veri akışı verileri önizlemesinin satır sınırı.</span><span class="sxs-lookup"><span data-stu-id="17268-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17268-140">-SessionID</span><span class="sxs-lookup"><span data-stu-id="17268-140">-SessionId</span></span>
<span data-ttu-id="17268-141">Veri akışı hata ayıklama oturum KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="17268-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17268-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="17268-142">-StreamName</span></span>
<span data-ttu-id="17268-143">Hata ayıklama için veri akışının akış adı.</span><span class="sxs-lookup"><span data-stu-id="17268-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17268-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="17268-144">-Confirm</span></span>
<span data-ttu-id="17268-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17268-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17268-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17268-146">-WhatIf</span></span>
<span data-ttu-id="17268-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17268-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17268-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17268-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17268-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17268-149">CommonParameters</span></span>
<span data-ttu-id="17268-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17268-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17268-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="17268-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17268-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17268-152">INPUTS</span></span>

### <span data-ttu-id="17268-153">System. String</span><span class="sxs-lookup"><span data-stu-id="17268-153">System.String</span></span>

### <span data-ttu-id="17268-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="17268-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="17268-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17268-155">OUTPUTS</span></span>

### <span data-ttu-id="17268-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="17268-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="17268-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17268-157">NOTES</span></span>
<span data-ttu-id="17268-158">Anahtar sözcükler: Azure, azurerm, ARM, Resource, yönetim, Manager, veri, factoriesKeywords</span><span class="sxs-lookup"><span data-stu-id="17268-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="17268-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17268-159">RELATED LINKS</span></span>

[<span data-ttu-id="17268-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="17268-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="17268-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="17268-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="17268-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="17268-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="17268-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="17268-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
