---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 98b34b4926dc4edc15d30308b2d6bfee33336f0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752439"
---
# <span data-ttu-id="532a3-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="532a3-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="532a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="532a3-102">SYNOPSIS</span></span>
<span data-ttu-id="532a3-103">Azure Veri Fabrikası 'nde veri akışı hata ayıklama oturumu başlatır</span><span class="sxs-lookup"><span data-stu-id="532a3-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="532a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="532a3-104">SYNTAX</span></span>

### <span data-ttu-id="532a3-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="532a3-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532a3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="532a3-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="532a3-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="532a3-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="532a3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="532a3-108">DESCRIPTION</span></span>
<span data-ttu-id="532a3-109">Bu uzun süre çalışan komut yaklaşan hata ayıklama komutları için veri akışı hata ayıklama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="532a3-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="532a3-110">Bu komut, hata ayıklama oturumu kümesinin boyutunu/türünü yapılandırmak için Integration Runtime tanımıyla birlikte iliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="532a3-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="532a3-111">Veri akışı hata ayıklama iş akışı için PowerShell komut dizisi:</span><span class="sxs-lookup"><span data-stu-id="532a3-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="532a3-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="532a3-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="532a3-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="532a3-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="532a3-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (Bu adımı farklı komutlar/hedefler için tekrarlama veya paket dosyasını değiştirmek için 2-3 adımını tekrarlama)</span><span class="sxs-lookup"><span data-stu-id="532a3-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="532a3-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="532a3-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="532a3-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="532a3-116">EXAMPLES</span></span>

### <span data-ttu-id="532a3-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="532a3-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="532a3-118">AsJob bayrağıyla bir hata ayıklama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="532a3-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="532a3-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="532a3-119">PARAMETERS</span></span>

### <span data-ttu-id="532a3-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="532a3-120">-AsJob</span></span>
<span data-ttu-id="532a3-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="532a3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="532a3-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="532a3-122">-DataFactory</span></span>
<span data-ttu-id="532a3-123">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="532a3-123">The data factory object.</span></span>

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

### <span data-ttu-id="532a3-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="532a3-124">-DataFactoryName</span></span>
<span data-ttu-id="532a3-125">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="532a3-125">The data factory name.</span></span>

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

### <span data-ttu-id="532a3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532a3-126">-DefaultProfile</span></span>
<span data-ttu-id="532a3-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="532a3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="532a3-128">-Integrationruntimefile</span><span class="sxs-lookup"><span data-stu-id="532a3-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="532a3-129">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="532a3-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="532a3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="532a3-130">-ResourceGroupName</span></span>
<span data-ttu-id="532a3-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="532a3-131">The resource group name.</span></span>

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

### <span data-ttu-id="532a3-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="532a3-132">-ResourceId</span></span>
<span data-ttu-id="532a3-133">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="532a3-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="532a3-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="532a3-134">-Confirm</span></span>
<span data-ttu-id="532a3-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="532a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="532a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="532a3-136">-WhatIf</span></span>
<span data-ttu-id="532a3-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="532a3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="532a3-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="532a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="532a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532a3-139">CommonParameters</span></span>
<span data-ttu-id="532a3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="532a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532a3-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="532a3-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532a3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="532a3-142">INPUTS</span></span>

### <span data-ttu-id="532a3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="532a3-143">System.String</span></span>

### <span data-ttu-id="532a3-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="532a3-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="532a3-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="532a3-145">OUTPUTS</span></span>

### <span data-ttu-id="532a3-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="532a3-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="532a3-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="532a3-147">NOTES</span></span>
<span data-ttu-id="532a3-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="532a3-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="532a3-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="532a3-149">RELATED LINKS</span></span>

[<span data-ttu-id="532a3-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="532a3-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="532a3-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="532a3-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="532a3-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="532a3-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="532a3-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="532a3-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)