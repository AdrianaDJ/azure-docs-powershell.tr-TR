---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278455"
---
# <span data-ttu-id="ec268-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="ec268-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="ec268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec268-102">SYNOPSIS</span></span>
<span data-ttu-id="ec268-103">Çalışma alanındaki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ec268-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="ec268-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec268-104">SYNTAX</span></span>

### <span data-ttu-id="ec268-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec268-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec268-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="ec268-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec268-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec268-107">DESCRIPTION</span></span>
<span data-ttu-id="ec268-108">**Get-AzSynapsePipeline** cmdlet 'i çalışma alanındaki ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ec268-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="ec268-109">Bir ardışık düzenin adını belirtirseniz, bu cmdlet bu ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ec268-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="ec268-110">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ec268-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="ec268-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec268-111">EXAMPLES</span></span>

### <span data-ttu-id="ec268-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec268-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ec268-113">Bu komut, ContosoWorkspace adlı çalışma alanındaki tüm ardışık düzenler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ec268-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ec268-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ec268-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="ec268-115">Bu komut, ContosoWorkspace adındaki çalışma alanında ContosoPipeline adlı ardışık düzen hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ec268-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ec268-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ec268-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="ec268-117">Bu komut, çalışma alanında ContosoPipeline adlı ardışık düzen ile ardışık düzen aracılığıyla bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ec268-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ec268-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec268-118">PARAMETERS</span></span>

### <span data-ttu-id="ec268-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec268-119">-DefaultProfile</span></span>
<span data-ttu-id="ec268-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec268-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec268-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec268-121">-Name</span></span>
<span data-ttu-id="ec268-122">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="ec268-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec268-123">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ec268-123">-WorkspaceName</span></span>
<span data-ttu-id="ec268-124">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ec268-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec268-125">-</span><span class="sxs-lookup"><span data-stu-id="ec268-125">-WorkspaceObject</span></span>
<span data-ttu-id="ec268-126">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ec268-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec268-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec268-127">CommonParameters</span></span>
<span data-ttu-id="ec268-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec268-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec268-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec268-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec268-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec268-130">INPUTS</span></span>

### <span data-ttu-id="ec268-131">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ec268-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ec268-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec268-132">OUTPUTS</span></span>

### <span data-ttu-id="ec268-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="ec268-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="ec268-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec268-134">NOTES</span></span>

## <span data-ttu-id="ec268-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec268-135">RELATED LINKS</span></span>
