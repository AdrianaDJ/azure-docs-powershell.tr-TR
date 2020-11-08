---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277137"
---
# <span data-ttu-id="257a8-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="257a8-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="257a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="257a8-102">SYNOPSIS</span></span>
<span data-ttu-id="257a8-103">SYNAPSE Analytics SQL havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="257a8-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="257a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="257a8-104">SYNTAX</span></span>

### <span data-ttu-id="257a8-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="257a8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257a8-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="257a8-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257a8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="257a8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257a8-108">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="257a8-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="257a8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="257a8-109">DESCRIPTION</span></span>
<span data-ttu-id="257a8-110">**Remove-AzSynapseSqlPool** cmdlet 'i, bir Azure SYNAPSE Analytics SQL havuzunu kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="257a8-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="257a8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="257a8-111">EXAMPLES</span></span>

### <span data-ttu-id="257a8-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="257a8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="257a8-113">Bu komut bir Azure SYNAPSE Analytics SQL havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="257a8-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="257a8-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="257a8-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="257a8-115">Bu komut bir Azure SYNAPSE Analytics SQL havuzunu ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="257a8-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="257a8-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="257a8-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="257a8-117">Bu komut bir Azure SYNAPSE Analytics SQL havuzunu ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="257a8-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="257a8-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="257a8-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="257a8-119">Bu komut, belirtilen kaynak KIMLIĞIYLE bir Azure SYNAPSE Analytics SQL havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="257a8-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="257a8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="257a8-120">PARAMETERS</span></span>

### <span data-ttu-id="257a8-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="257a8-121">-AsJob</span></span>
<span data-ttu-id="257a8-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="257a8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="257a8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257a8-123">-DefaultProfile</span></span>
<span data-ttu-id="257a8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="257a8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="257a8-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="257a8-125">-InputObject</span></span>
<span data-ttu-id="257a8-126">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="257a8-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="257a8-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="257a8-127">-Name</span></span>
<span data-ttu-id="257a8-128">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="257a8-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257a8-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="257a8-129">-PassThru</span></span>
<span data-ttu-id="257a8-130">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="257a8-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="257a8-131">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="257a8-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="257a8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257a8-132">-ResourceGroupName</span></span>
<span data-ttu-id="257a8-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="257a8-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257a8-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="257a8-134">-ResourceId</span></span>
<span data-ttu-id="257a8-135">SYNAPSE SQL havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="257a8-135">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257a8-136">-Version</span><span class="sxs-lookup"><span data-stu-id="257a8-136">-Version</span></span>
<span data-ttu-id="257a8-137">SYNAPSE SQL havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="257a8-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="257a8-138">Örneğin, 2 veya 3.</span><span class="sxs-lookup"><span data-stu-id="257a8-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="257a8-139">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="257a8-139">-WorkspaceName</span></span>
<span data-ttu-id="257a8-140">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="257a8-140">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257a8-141">-</span><span class="sxs-lookup"><span data-stu-id="257a8-141">-WorkspaceObject</span></span>
<span data-ttu-id="257a8-142">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="257a8-142">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="257a8-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="257a8-143">-Confirm</span></span>
<span data-ttu-id="257a8-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="257a8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="257a8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257a8-145">-WhatIf</span></span>
<span data-ttu-id="257a8-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="257a8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257a8-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="257a8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="257a8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257a8-148">CommonParameters</span></span>
<span data-ttu-id="257a8-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="257a8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257a8-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="257a8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257a8-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="257a8-151">INPUTS</span></span>

### <span data-ttu-id="257a8-152">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="257a8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="257a8-153">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="257a8-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="257a8-154">System. String</span><span class="sxs-lookup"><span data-stu-id="257a8-154">System.String</span></span>

## <span data-ttu-id="257a8-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="257a8-155">OUTPUTS</span></span>

### <span data-ttu-id="257a8-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="257a8-156">System.Boolean</span></span>

## <span data-ttu-id="257a8-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="257a8-157">NOTES</span></span>

## <span data-ttu-id="257a8-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="257a8-158">RELATED LINKS</span></span>
