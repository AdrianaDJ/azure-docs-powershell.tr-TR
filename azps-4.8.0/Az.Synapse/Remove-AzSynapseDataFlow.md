---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: dcfcd391d1103b0755a3ffae481e4f1bd5fde2c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109917"
---
# <span data-ttu-id="bab0d-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="bab0d-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="bab0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bab0d-102">SYNOPSIS</span></span>
<span data-ttu-id="bab0d-103">Çalışma alanından veri akışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bab0d-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="bab0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bab0d-104">SYNTAX</span></span>

### <span data-ttu-id="bab0d-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bab0d-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bab0d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="bab0d-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bab0d-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="bab0d-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bab0d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bab0d-108">DESCRIPTION</span></span>
<span data-ttu-id="bab0d-109">**Remove-AzSynapseDataFlow** cmdlet 'i çalışma alanından veri akışını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bab0d-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="bab0d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bab0d-110">EXAMPLES</span></span>

### <span data-ttu-id="bab0d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bab0d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="bab0d-112">Bu komut, ContosoDataFlow adlı veri akışını ContosoWorkspace adlı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bab0d-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="bab0d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bab0d-113">PARAMETERS</span></span>

### <span data-ttu-id="bab0d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="bab0d-114">-AsJob</span></span>
<span data-ttu-id="bab0d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bab0d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bab0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab0d-116">-DefaultProfile</span></span>
<span data-ttu-id="bab0d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bab0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bab0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bab0d-118">-InputObject</span></span>
<span data-ttu-id="bab0d-119">Veri akışı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bab0d-119">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bab0d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bab0d-120">-Name</span></span>
<span data-ttu-id="bab0d-121">Veri akışı adı.</span><span class="sxs-lookup"><span data-stu-id="bab0d-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab0d-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bab0d-122">-PassThru</span></span>
<span data-ttu-id="bab0d-123">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bab0d-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bab0d-124">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="bab0d-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bab0d-125">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="bab0d-125">-WorkspaceName</span></span>
<span data-ttu-id="bab0d-126">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="bab0d-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bab0d-127">-</span><span class="sxs-lookup"><span data-stu-id="bab0d-127">-WorkspaceObject</span></span>
<span data-ttu-id="bab0d-128">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="bab0d-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bab0d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bab0d-129">-Confirm</span></span>
<span data-ttu-id="bab0d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bab0d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bab0d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab0d-131">-WhatIf</span></span>
<span data-ttu-id="bab0d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bab0d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bab0d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bab0d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bab0d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab0d-134">CommonParameters</span></span>
<span data-ttu-id="bab0d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bab0d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab0d-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bab0d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab0d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bab0d-137">INPUTS</span></span>

### <span data-ttu-id="bab0d-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bab0d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bab0d-139">Microsoft.Azure.Commands.Synapse.Models.PSDAtaakışkaynağı</span><span class="sxs-lookup"><span data-stu-id="bab0d-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="bab0d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bab0d-140">OUTPUTS</span></span>

### <span data-ttu-id="bab0d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bab0d-141">System.Boolean</span></span>

## <span data-ttu-id="bab0d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bab0d-142">NOTES</span></span>

## <span data-ttu-id="bab0d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bab0d-143">RELATED LINKS</span></span>
