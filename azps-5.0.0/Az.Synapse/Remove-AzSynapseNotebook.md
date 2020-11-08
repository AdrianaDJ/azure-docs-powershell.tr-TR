---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277928"
---
# <span data-ttu-id="1081a-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="1081a-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="1081a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1081a-102">SYNOPSIS</span></span>
<span data-ttu-id="1081a-103">Bir çalışma alanından Not defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1081a-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="1081a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1081a-104">SYNTAX</span></span>

### <span data-ttu-id="1081a-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1081a-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1081a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="1081a-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1081a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="1081a-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1081a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1081a-108">DESCRIPTION</span></span>
<span data-ttu-id="1081a-109">**Remove-AzSynapseNotebook** cmdlet 'i çalışma alanından bir not defterini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1081a-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="1081a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1081a-110">EXAMPLES</span></span>

### <span data-ttu-id="1081a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1081a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="1081a-112">Çalışma alanı olan ContosoNotebook adındaki bir not defterini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="1081a-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="1081a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1081a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="1081a-114">Çalışma alanı 'nda ContosoNotebook adındaki bir not defterini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="1081a-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="1081a-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1081a-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="1081a-116">Çalışma alanı 'nda ContosoNotebook adındaki bir not defterini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="1081a-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1081a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1081a-117">PARAMETERS</span></span>

### <span data-ttu-id="1081a-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="1081a-118">-AsJob</span></span>
<span data-ttu-id="1081a-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1081a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1081a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1081a-120">-DefaultProfile</span></span>
<span data-ttu-id="1081a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1081a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1081a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1081a-122">-InputObject</span></span>
<span data-ttu-id="1081a-123">Not defteri nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1081a-123">The notebook object.</span></span>

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

### <span data-ttu-id="1081a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1081a-124">-Name</span></span>
<span data-ttu-id="1081a-125">Not defteri adı.</span><span class="sxs-lookup"><span data-stu-id="1081a-125">The notebook name.</span></span>

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

### <span data-ttu-id="1081a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1081a-126">-PassThru</span></span>
<span data-ttu-id="1081a-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="1081a-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1081a-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="1081a-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1081a-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="1081a-129">-WorkspaceName</span></span>
<span data-ttu-id="1081a-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="1081a-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1081a-131">-</span><span class="sxs-lookup"><span data-stu-id="1081a-131">-WorkspaceObject</span></span>
<span data-ttu-id="1081a-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="1081a-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1081a-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="1081a-133">-Confirm</span></span>
<span data-ttu-id="1081a-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1081a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1081a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1081a-135">-WhatIf</span></span>
<span data-ttu-id="1081a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1081a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1081a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1081a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1081a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1081a-138">CommonParameters</span></span>
<span data-ttu-id="1081a-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1081a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1081a-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1081a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1081a-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1081a-141">INPUTS</span></span>

### <span data-ttu-id="1081a-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1081a-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1081a-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="1081a-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="1081a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1081a-144">OUTPUTS</span></span>

### <span data-ttu-id="1081a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1081a-145">System.Boolean</span></span>

## <span data-ttu-id="1081a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1081a-146">NOTES</span></span>

## <span data-ttu-id="1081a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1081a-147">RELATED LINKS</span></span>
