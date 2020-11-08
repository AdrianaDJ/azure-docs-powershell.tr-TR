---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110131"
---
# <span data-ttu-id="0e76b-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0e76b-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="0e76b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e76b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e76b-103">SYNAPSE Analytics Spark havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="0e76b-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="0e76b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e76b-104">SYNTAX</span></span>

### <span data-ttu-id="0e76b-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0e76b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e76b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e76b-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e76b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e76b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e76b-108">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0e76b-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e76b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e76b-109">DESCRIPTION</span></span>
<span data-ttu-id="0e76b-110">**Remove-AzSynapseSparkPool** cmdlet 'ı bir Azure SYNAPSE Analytics Spark havuzunu kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="0e76b-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="0e76b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e76b-111">EXAMPLES</span></span>

### <span data-ttu-id="0e76b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0e76b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="0e76b-113">Bu komut bir Azure SYNAPSE Analytics Spark havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="0e76b-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="0e76b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0e76b-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="0e76b-115">Bu komut bir Azure SYNAPSE Analytics Spark havuzunu ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="0e76b-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="0e76b-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0e76b-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="0e76b-117">Bu komut bir Azure SYNAPSE Analytics Spark havuzunu ardışık düzen aracılığıyla siler.</span><span class="sxs-lookup"><span data-stu-id="0e76b-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="0e76b-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="0e76b-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="0e76b-119">Bu komut, kaynak KIMLIĞIYLE bir Azure SYNAPSE Analytics Spark havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="0e76b-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="0e76b-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e76b-120">PARAMETERS</span></span>

### <span data-ttu-id="0e76b-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="0e76b-121">-AsJob</span></span>
<span data-ttu-id="0e76b-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0e76b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e76b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e76b-123">-DefaultProfile</span></span>
<span data-ttu-id="0e76b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e76b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e76b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e76b-125">-InputObject</span></span>
<span data-ttu-id="0e76b-126">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0e76b-126">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e76b-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e76b-127">-Name</span></span>
<span data-ttu-id="0e76b-128">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="0e76b-128">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e76b-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0e76b-129">-PassThru</span></span>
<span data-ttu-id="0e76b-130">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="0e76b-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0e76b-131">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="0e76b-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0e76b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e76b-132">-ResourceGroupName</span></span>
<span data-ttu-id="0e76b-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0e76b-133">Resource group name.</span></span>

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

### <span data-ttu-id="0e76b-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0e76b-134">-ResourceId</span></span>
<span data-ttu-id="0e76b-135">SYNAPSE Spark havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="0e76b-135">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e76b-136">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="0e76b-136">-WorkspaceName</span></span>
<span data-ttu-id="0e76b-137">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="0e76b-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0e76b-138">-</span><span class="sxs-lookup"><span data-stu-id="0e76b-138">-WorkspaceObject</span></span>
<span data-ttu-id="0e76b-139">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="0e76b-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0e76b-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e76b-140">-Confirm</span></span>
<span data-ttu-id="0e76b-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e76b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e76b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e76b-142">-WhatIf</span></span>
<span data-ttu-id="0e76b-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e76b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e76b-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e76b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e76b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e76b-145">CommonParameters</span></span>
<span data-ttu-id="0e76b-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e76b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e76b-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0e76b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e76b-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e76b-148">INPUTS</span></span>

### <span data-ttu-id="0e76b-149">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e76b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0e76b-150">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0e76b-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="0e76b-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e76b-151">OUTPUTS</span></span>

### <span data-ttu-id="0e76b-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e76b-152">System.Boolean</span></span>

## <span data-ttu-id="0e76b-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e76b-153">NOTES</span></span>

## <span data-ttu-id="0e76b-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e76b-154">RELATED LINKS</span></span>
