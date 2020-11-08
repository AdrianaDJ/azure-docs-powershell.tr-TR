---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268935"
---
# <span data-ttu-id="ca1ae-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ca1ae-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="ca1ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1ae-103">SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ca1ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca1ae-104">SYNTAX</span></span>

### <span data-ttu-id="ca1ae-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca1ae-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-112">Pausebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ca1ae-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-114">Resumebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ca1ae-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1ae-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca1ae-116">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ca1ae-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca1ae-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca1ae-117">DESCRIPTION</span></span>
<span data-ttu-id="ca1ae-118">**Update-AzSynapseSqlPool** cmdlet 'ı bir Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ca1ae-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca1ae-119">EXAMPLES</span></span>

### <span data-ttu-id="ca1ae-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca1ae-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="ca1ae-121">Bu komut, bir Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="ca1ae-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ca1ae-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="ca1ae-123">Bu komut, ardışık düzen aracılığıyla Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="ca1ae-124">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ca1ae-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="ca1ae-125">Bu komut, ardışık düzen aracılığıyla Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="ca1ae-126">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="ca1ae-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="ca1ae-127">Bu komut, kaynak KIMLIĞIYLE bir Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="ca1ae-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca1ae-128">PARAMETERS</span></span>

### <span data-ttu-id="ca1ae-129">-Iş</span><span class="sxs-lookup"><span data-stu-id="ca1ae-129">-AsJob</span></span>
<span data-ttu-id="ca1ae-130">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ca1ae-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca1ae-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1ae-131">-DefaultProfile</span></span>
<span data-ttu-id="ca1ae-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca1ae-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca1ae-133">-InputObject</span></span>
<span data-ttu-id="ca1ae-134">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca1ae-135">-Name</span></span>
<span data-ttu-id="ca1ae-136">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-137">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ca1ae-137">-PassThru</span></span>
<span data-ttu-id="ca1ae-138">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ca1ae-139">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ca1ae-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="ca1ae-140">-PerformanceLevel</span></span>
<span data-ttu-id="ca1ae-141">SQL havuzuna atanacak SQL hizmet katmanı ve performans düzeyi.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="ca1ae-142">Örneğin, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca1ae-143">-ResourceGroupName</span></span>
<span data-ttu-id="ca1ae-144">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ca1ae-145">-ResourceId</span></span>
<span data-ttu-id="ca1ae-146">SYNAPSE SQL havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-147">-Özgeçmiş</span><span class="sxs-lookup"><span data-stu-id="ca1ae-147">-Resume</span></span>
<span data-ttu-id="ca1ae-148">SQL havuzunun devam ettiğini gösterir</span><span class="sxs-lookup"><span data-stu-id="ca1ae-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-149">-Askıya al</span><span class="sxs-lookup"><span data-stu-id="ca1ae-149">-Suspend</span></span>
<span data-ttu-id="ca1ae-150">SQL havuzunun duraklatılacağını gösterir</span><span class="sxs-lookup"><span data-stu-id="ca1ae-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-151">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ca1ae-151">-Tag</span></span>
<span data-ttu-id="ca1ae-152">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-153">-Version</span><span class="sxs-lookup"><span data-stu-id="ca1ae-153">-Version</span></span>
<span data-ttu-id="ca1ae-154">SYNAPSE SQL havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="ca1ae-155">Örneğin, 2 veya 3.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-155">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-156">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ca1ae-156">-WorkspaceName</span></span>
<span data-ttu-id="ca1ae-157">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-158">-</span><span class="sxs-lookup"><span data-stu-id="ca1ae-158">-WorkspaceObject</span></span>
<span data-ttu-id="ca1ae-159">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ae-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca1ae-160">-Confirm</span></span>
<span data-ttu-id="ca1ae-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca1ae-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1ae-162">-WhatIf</span></span>
<span data-ttu-id="ca1ae-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca1ae-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca1ae-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1ae-165">CommonParameters</span></span>
<span data-ttu-id="ca1ae-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1ae-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca1ae-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1ae-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca1ae-168">INPUTS</span></span>

### <span data-ttu-id="ca1ae-169">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ca1ae-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ca1ae-170">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ca1ae-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ca1ae-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca1ae-171">OUTPUTS</span></span>

### <span data-ttu-id="ca1ae-172">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ca1ae-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ca1ae-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca1ae-173">NOTES</span></span>

## <span data-ttu-id="ca1ae-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca1ae-174">RELATED LINKS</span></span>
