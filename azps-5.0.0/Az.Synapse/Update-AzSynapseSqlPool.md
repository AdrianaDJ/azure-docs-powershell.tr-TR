---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276315"
---
# <span data-ttu-id="11e01-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="11e01-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="11e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e01-102">SYNOPSIS</span></span>
<span data-ttu-id="11e01-103">SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="11e01-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="11e01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11e01-104">SYNTAX</span></span>

### <span data-ttu-id="11e01-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="11e01-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e01-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e01-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e01-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e01-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e01-108">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="11e01-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e01-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="11e01-109">DESCRIPTION</span></span>
<span data-ttu-id="11e01-110">**Update-AzSynapseSqlPool** cmdlet 'ı bir Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="11e01-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="11e01-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11e01-111">EXAMPLES</span></span>

### <span data-ttu-id="11e01-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11e01-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="11e01-113">Bu komut, bir Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="11e01-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="11e01-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="11e01-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="11e01-115">Bu komut, ardışık düzen aracılığıyla Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="11e01-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="11e01-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="11e01-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="11e01-117">Bu komut, ardışık düzen aracılığıyla Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="11e01-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="11e01-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="11e01-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="11e01-119">Bu komut, kaynak KIMLIĞIYLE bir Azure SYNAPSE Analytics SQL havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="11e01-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="11e01-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11e01-120">PARAMETERS</span></span>

### <span data-ttu-id="11e01-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="11e01-121">-AsJob</span></span>
<span data-ttu-id="11e01-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="11e01-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11e01-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e01-123">-DefaultProfile</span></span>
<span data-ttu-id="11e01-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11e01-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e01-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e01-125">-InputObject</span></span>
<span data-ttu-id="11e01-126">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="11e01-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="11e01-127">-Name</span></span>
<span data-ttu-id="11e01-128">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="11e01-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="11e01-129">-PassThru</span></span>
<span data-ttu-id="11e01-130">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="11e01-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="11e01-131">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="11e01-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="11e01-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="11e01-132">-PerformanceLevel</span></span>
<span data-ttu-id="11e01-133">SQL havuzuna atanacak SQL hizmet katmanı ve performans düzeyi.</span><span class="sxs-lookup"><span data-stu-id="11e01-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="11e01-134">Örneğin, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="11e01-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e01-135">-ResourceGroupName</span></span>
<span data-ttu-id="11e01-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="11e01-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="11e01-137">-ResourceId</span></span>
<span data-ttu-id="11e01-138">SYNAPSE SQL havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="11e01-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="11e01-139">-Tag</span></span>
<span data-ttu-id="11e01-140">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="11e01-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-141">-Version</span><span class="sxs-lookup"><span data-stu-id="11e01-141">-Version</span></span>
<span data-ttu-id="11e01-142">SYNAPSE SQL havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="11e01-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="11e01-143">Örneğin, 2 veya 3.</span><span class="sxs-lookup"><span data-stu-id="11e01-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="11e01-144">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="11e01-144">-WorkspaceName</span></span>
<span data-ttu-id="11e01-145">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="11e01-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-146">-</span><span class="sxs-lookup"><span data-stu-id="11e01-146">-WorkspaceObject</span></span>
<span data-ttu-id="11e01-147">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="11e01-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e01-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="11e01-148">-Confirm</span></span>
<span data-ttu-id="11e01-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11e01-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e01-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e01-150">-WhatIf</span></span>
<span data-ttu-id="11e01-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11e01-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e01-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11e01-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e01-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e01-153">CommonParameters</span></span>
<span data-ttu-id="11e01-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11e01-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e01-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="11e01-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e01-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11e01-156">INPUTS</span></span>

### <span data-ttu-id="11e01-157">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11e01-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="11e01-158">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="11e01-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="11e01-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11e01-159">OUTPUTS</span></span>

### <span data-ttu-id="11e01-160">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="11e01-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="11e01-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11e01-161">NOTES</span></span>

## <span data-ttu-id="11e01-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11e01-162">RELATED LINKS</span></span>
