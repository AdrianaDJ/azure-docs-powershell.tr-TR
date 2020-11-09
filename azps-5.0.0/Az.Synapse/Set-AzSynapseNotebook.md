---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324862"
---
# <span data-ttu-id="5902b-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="5902b-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="5902b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5902b-102">SYNOPSIS</span></span>
<span data-ttu-id="5902b-103">Çalışma alanında Not defteri oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5902b-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="5902b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5902b-104">SYNTAX</span></span>

### <span data-ttu-id="5902b-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5902b-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5902b-106">Setbinaik Cümini havuz</span><span class="sxs-lookup"><span data-stu-id="5902b-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5902b-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="5902b-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5902b-108">Setbyobjectandparlak havuz</span><span class="sxs-lookup"><span data-stu-id="5902b-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5902b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5902b-109">DESCRIPTION</span></span>
<span data-ttu-id="5902b-110">**Set-AzSynapseNotebook** cmdlet 'i çalışma alanında bir not defteri oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5902b-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="5902b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5902b-111">EXAMPLES</span></span>

### <span data-ttu-id="5902b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5902b-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="5902b-113">Bu komut, bir not defteri dosya Not defteri (contoso</span><span class="sxs-lookup"><span data-stu-id="5902b-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="5902b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5902b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="5902b-115">Bu komut, çalışma alanı ardışık düzen aracılığıyla, çalışma alanındaki Not defteri dosya Not defteri</span><span class="sxs-lookup"><span data-stu-id="5902b-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="5902b-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5902b-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="5902b-117">Bu komut, Not defteri dosya Not defteri 'nden bir not defteri oluşturur veya bu not defterini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="5902b-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="5902b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5902b-118">PARAMETERS</span></span>

### <span data-ttu-id="5902b-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="5902b-119">-AsJob</span></span>
<span data-ttu-id="5902b-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5902b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5902b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5902b-121">-DefaultProfile</span></span>
<span data-ttu-id="5902b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5902b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5902b-123">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="5902b-123">-DefinitionFile</span></span>
<span data-ttu-id="5902b-124">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="5902b-124">The JSON file path.</span></span>

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

### <span data-ttu-id="5902b-125">-Yürüttorsayısı</span><span class="sxs-lookup"><span data-stu-id="5902b-125">-ExecutorCount</span></span>
<span data-ttu-id="5902b-126">İş için belirtilen Spark havuzunda ayrılacak yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="5902b-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5902b-127">-Yürüttorsize</span><span class="sxs-lookup"><span data-stu-id="5902b-127">-ExecutorSize</span></span>
<span data-ttu-id="5902b-128">İş için belirtilen Spark havuzunda tahsis edilen yürüticileri için kullanılacak çekirdek ve bellek sayısı.</span><span class="sxs-lookup"><span data-stu-id="5902b-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5902b-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="5902b-129">-Name</span></span>
<span data-ttu-id="5902b-130">Not defteri adı.</span><span class="sxs-lookup"><span data-stu-id="5902b-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5902b-131">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="5902b-131">-SparkPoolName</span></span>
<span data-ttu-id="5902b-132">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="5902b-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5902b-133">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="5902b-133">-WorkspaceName</span></span>
<span data-ttu-id="5902b-134">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="5902b-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5902b-135">-</span><span class="sxs-lookup"><span data-stu-id="5902b-135">-WorkspaceObject</span></span>
<span data-ttu-id="5902b-136">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="5902b-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5902b-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="5902b-137">-Confirm</span></span>
<span data-ttu-id="5902b-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5902b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5902b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5902b-139">-WhatIf</span></span>
<span data-ttu-id="5902b-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5902b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5902b-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5902b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5902b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5902b-142">CommonParameters</span></span>
<span data-ttu-id="5902b-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5902b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5902b-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5902b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5902b-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5902b-145">INPUTS</span></span>

### <span data-ttu-id="5902b-146">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5902b-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5902b-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5902b-147">OUTPUTS</span></span>

### <span data-ttu-id="5902b-148">Microsoft. Azure. Commands. SYNAPSE. modeller. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="5902b-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="5902b-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5902b-149">NOTES</span></span>

## <span data-ttu-id="5902b-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5902b-150">RELATED LINKS</span></span>
