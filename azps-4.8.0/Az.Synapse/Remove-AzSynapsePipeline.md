---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109909"
---
# <span data-ttu-id="839ea-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="839ea-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="839ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="839ea-102">SYNOPSIS</span></span>
<span data-ttu-id="839ea-103">Bir ardışık düzeni çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="839ea-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="839ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="839ea-104">SYNTAX</span></span>

### <span data-ttu-id="839ea-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="839ea-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="839ea-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="839ea-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="839ea-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="839ea-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="839ea-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="839ea-108">DESCRIPTION</span></span>
<span data-ttu-id="839ea-109">**Remove-AzSynapsePipeline** cmdlet 'i çalışma alanından ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="839ea-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="839ea-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="839ea-110">EXAMPLES</span></span>

### <span data-ttu-id="839ea-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="839ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="839ea-112">Bu cmdlet, ContosoPipeline adındaki ardışık düzeni ContosoWorkspace adındaki çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="839ea-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="839ea-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="839ea-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="839ea-114">Bu cmdlet, ContosoPipeline adlı ardışık düzeni, ContosoWorkspace aracılığıyla, ardışık düzen aracılığıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="839ea-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="839ea-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="839ea-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="839ea-116">Bu cmdlet, ContosoPipeline adlı ardışık düzeni, ContosoWorkspace aracılığıyla, ardışık düzen aracılığıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="839ea-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="839ea-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="839ea-117">PARAMETERS</span></span>

### <span data-ttu-id="839ea-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="839ea-118">-AsJob</span></span>
<span data-ttu-id="839ea-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="839ea-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="839ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839ea-120">-DefaultProfile</span></span>
<span data-ttu-id="839ea-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="839ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="839ea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="839ea-122">-InputObject</span></span>
<span data-ttu-id="839ea-123">Boru hattı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="839ea-123">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="839ea-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="839ea-124">-Name</span></span>
<span data-ttu-id="839ea-125">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="839ea-125">The pipeline name.</span></span>

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

### <span data-ttu-id="839ea-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="839ea-126">-PassThru</span></span>
<span data-ttu-id="839ea-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="839ea-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="839ea-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="839ea-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="839ea-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="839ea-129">-WorkspaceName</span></span>
<span data-ttu-id="839ea-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="839ea-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839ea-131">-</span><span class="sxs-lookup"><span data-stu-id="839ea-131">-WorkspaceObject</span></span>
<span data-ttu-id="839ea-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="839ea-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="839ea-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="839ea-133">-Confirm</span></span>
<span data-ttu-id="839ea-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="839ea-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="839ea-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="839ea-135">-WhatIf</span></span>
<span data-ttu-id="839ea-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="839ea-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="839ea-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="839ea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="839ea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839ea-138">CommonParameters</span></span>
<span data-ttu-id="839ea-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="839ea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839ea-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="839ea-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839ea-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="839ea-141">INPUTS</span></span>

### <span data-ttu-id="839ea-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="839ea-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="839ea-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="839ea-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="839ea-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="839ea-144">OUTPUTS</span></span>

### <span data-ttu-id="839ea-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="839ea-145">System.Boolean</span></span>

## <span data-ttu-id="839ea-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="839ea-146">NOTES</span></span>

## <span data-ttu-id="839ea-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="839ea-147">RELATED LINKS</span></span>
