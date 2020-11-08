---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277905"
---
# <span data-ttu-id="6768c-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="6768c-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="6768c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6768c-102">SYNOPSIS</span></span>
<span data-ttu-id="6768c-103">Çalışma alanında ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6768c-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="6768c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6768c-104">SYNTAX</span></span>

### <span data-ttu-id="6768c-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6768c-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6768c-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="6768c-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6768c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6768c-107">DESCRIPTION</span></span>
<span data-ttu-id="6768c-108">**Set-AzSynapsePipeline** cmdlet 'i çalışma alanında bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6768c-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="6768c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6768c-109">EXAMPLES</span></span>

### <span data-ttu-id="6768c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6768c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="6768c-111">Bu komut, ContosoWorkspace adlı çalışma alanında ContosoPipeline adlı bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6768c-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="6768c-112">Komut, ardışık düzeni pipeline.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="6768c-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="6768c-113">Bu dosya etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="6768c-113">This file includes information about activities.</span></span>

### <span data-ttu-id="6768c-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6768c-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="6768c-115">Bu komut, ContosoPipeline adında bir ardışık düzen oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6768c-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="6768c-116">Komut, ardışık düzeni pipeline.jsdosyadaki bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="6768c-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="6768c-117">Bu dosya etkinlikler hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="6768c-117">This file includes information about activities.</span></span>

## <span data-ttu-id="6768c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6768c-118">PARAMETERS</span></span>

### <span data-ttu-id="6768c-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="6768c-119">-AsJob</span></span>
<span data-ttu-id="6768c-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6768c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6768c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6768c-121">-DefaultProfile</span></span>
<span data-ttu-id="6768c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6768c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6768c-123">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="6768c-123">-DefinitionFile</span></span>
<span data-ttu-id="6768c-124">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="6768c-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6768c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="6768c-125">-Name</span></span>
<span data-ttu-id="6768c-126">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="6768c-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6768c-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="6768c-127">-WorkspaceName</span></span>
<span data-ttu-id="6768c-128">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="6768c-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6768c-129">-</span><span class="sxs-lookup"><span data-stu-id="6768c-129">-WorkspaceObject</span></span>
<span data-ttu-id="6768c-130">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="6768c-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6768c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6768c-131">-Confirm</span></span>
<span data-ttu-id="6768c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6768c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6768c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6768c-133">-WhatIf</span></span>
<span data-ttu-id="6768c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6768c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6768c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6768c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6768c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6768c-136">CommonParameters</span></span>
<span data-ttu-id="6768c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6768c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6768c-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6768c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6768c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6768c-139">INPUTS</span></span>

### <span data-ttu-id="6768c-140">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6768c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6768c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6768c-141">OUTPUTS</span></span>

### <span data-ttu-id="6768c-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="6768c-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="6768c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6768c-143">NOTES</span></span>

## <span data-ttu-id="6768c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6768c-144">RELATED LINKS</span></span>
