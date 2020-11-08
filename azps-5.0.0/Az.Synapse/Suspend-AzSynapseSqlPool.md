---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275163"
---
# <span data-ttu-id="ad3e4-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ad3e4-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="ad3e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3e4-103">SYNAPSE Analytics SQL havuzunu askıya alır.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ad3e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad3e4-104">SYNTAX</span></span>

### <span data-ttu-id="ad3e4-105">SuspendByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad3e4-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad3e4-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad3e4-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad3e4-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad3e4-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad3e4-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad3e4-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad3e4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad3e4-109">DESCRIPTION</span></span>
<span data-ttu-id="ad3e4-110">**Suspend-AzSynapseSqlPool** cmdlet 'ı bir Azure SYNAPSE Analytics SQL havuzunu askıya alır.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ad3e4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad3e4-111">EXAMPLES</span></span>

### <span data-ttu-id="ad3e4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ad3e4-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="ad3e4-113">Bu komut, etkin bir Azure SYNAPSE Analytics SQL havuzunu askıya alır.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ad3e4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad3e4-114">PARAMETERS</span></span>

### <span data-ttu-id="ad3e4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="ad3e4-115">-AsJob</span></span>
<span data-ttu-id="ad3e4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ad3e4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad3e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3e4-117">-DefaultProfile</span></span>
<span data-ttu-id="ad3e4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad3e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad3e4-119">-InputObject</span></span>
<span data-ttu-id="ad3e4-120">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3e4-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad3e4-121">-Name</span></span>
<span data-ttu-id="ad3e4-122">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3e4-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ad3e4-123">-PassThru</span></span>
<span data-ttu-id="ad3e4-124">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ad3e4-125">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ad3e4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3e4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad3e4-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3e4-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ad3e4-128">-ResourceId</span></span>
<span data-ttu-id="ad3e4-129">SYNAPSE SQL havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3e4-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ad3e4-130">-WorkspaceName</span></span>
<span data-ttu-id="ad3e4-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3e4-132">-</span><span class="sxs-lookup"><span data-stu-id="ad3e4-132">-WorkspaceObject</span></span>
<span data-ttu-id="ad3e4-133">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3e4-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad3e4-134">-Confirm</span></span>
<span data-ttu-id="ad3e4-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad3e4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad3e4-136">-WhatIf</span></span>
<span data-ttu-id="ad3e4-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad3e4-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad3e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3e4-139">CommonParameters</span></span>
<span data-ttu-id="ad3e4-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3e4-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ad3e4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3e4-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad3e4-142">INPUTS</span></span>

### <span data-ttu-id="ad3e4-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ad3e4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ad3e4-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ad3e4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ad3e4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad3e4-145">OUTPUTS</span></span>

### <span data-ttu-id="ad3e4-146">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ad3e4-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ad3e4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad3e4-147">NOTES</span></span>

## <span data-ttu-id="ad3e4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad3e4-148">RELATED LINKS</span></span>
