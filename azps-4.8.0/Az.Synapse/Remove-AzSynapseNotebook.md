---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109910"
---
# <span data-ttu-id="8badb-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="8badb-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="8badb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8badb-102">SYNOPSIS</span></span>
<span data-ttu-id="8badb-103">Bir çalışma alanından Not defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8badb-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="8badb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8badb-104">SYNTAX</span></span>

### <span data-ttu-id="8badb-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8badb-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8badb-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="8badb-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8badb-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="8badb-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8badb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8badb-108">DESCRIPTION</span></span>
<span data-ttu-id="8badb-109">**Remove-AzSynapseNotebook** cmdlet 'i çalışma alanından bir not defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8badb-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="8badb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8badb-110">EXAMPLES</span></span>

### <span data-ttu-id="8badb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8badb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="8badb-112">Çalışma alanı olan ContosoNotebook adındaki bir not defterini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="8badb-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="8badb-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8badb-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="8badb-114">Çalışma alanı 'nda ContosoNotebook adındaki bir not defterini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="8badb-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="8badb-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8badb-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="8badb-116">Çalışma alanı 'nda ContosoNotebook adındaki bir not defterini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="8badb-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="8badb-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8badb-117">PARAMETERS</span></span>

### <span data-ttu-id="8badb-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="8badb-118">-AsJob</span></span>
<span data-ttu-id="8badb-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8badb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8badb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8badb-120">-DefaultProfile</span></span>
<span data-ttu-id="8badb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8badb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8badb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8badb-122">-InputObject</span></span>
<span data-ttu-id="8badb-123">Not defteri nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8badb-123">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8badb-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8badb-124">-Name</span></span>
<span data-ttu-id="8badb-125">Not defteri adı.</span><span class="sxs-lookup"><span data-stu-id="8badb-125">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8badb-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8badb-126">-PassThru</span></span>
<span data-ttu-id="8badb-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="8badb-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8badb-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="8badb-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8badb-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="8badb-129">-WorkspaceName</span></span>
<span data-ttu-id="8badb-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="8badb-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8badb-131">-</span><span class="sxs-lookup"><span data-stu-id="8badb-131">-WorkspaceObject</span></span>
<span data-ttu-id="8badb-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="8badb-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8badb-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="8badb-133">-Confirm</span></span>
<span data-ttu-id="8badb-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8badb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8badb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8badb-135">-WhatIf</span></span>
<span data-ttu-id="8badb-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8badb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8badb-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8badb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8badb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8badb-138">CommonParameters</span></span>
<span data-ttu-id="8badb-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8badb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8badb-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8badb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8badb-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8badb-141">INPUTS</span></span>

### <span data-ttu-id="8badb-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8badb-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8badb-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="8badb-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="8badb-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8badb-144">OUTPUTS</span></span>

### <span data-ttu-id="8badb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8badb-145">System.Boolean</span></span>

## <span data-ttu-id="8badb-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8badb-146">NOTES</span></span>

## <span data-ttu-id="8badb-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8badb-147">RELATED LINKS</span></span>
