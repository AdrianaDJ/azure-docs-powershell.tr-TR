---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278453"
---
# <span data-ttu-id="f4724-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f4724-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="f4724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4724-102">SYNOPSIS</span></span>
<span data-ttu-id="f4724-103">SYNAPSE Analytics Spark havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4724-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f4724-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4724-104">SYNTAX</span></span>

### <span data-ttu-id="f4724-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4724-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4724-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4724-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4724-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4724-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4724-108">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f4724-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4724-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4724-109">DESCRIPTION</span></span>
<span data-ttu-id="f4724-110">**Update-AzSynapseSparkPool** cmdlet 'ı bir Azure SYNAPSE Analytics Spark havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4724-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f4724-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4724-111">EXAMPLES</span></span>

### <span data-ttu-id="f4724-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4724-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="f4724-113">Bu komut, bir Azure SYNAPSE Analytics Spark havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4724-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f4724-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f4724-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="f4724-115">Bu komut, bir Azure SYNAPSE Analytics Spark havuzunu ardışık düzen aracılığıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4724-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="f4724-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f4724-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="f4724-117">Bu komut, bir Azure SYNAPSE Analytics Spark havuzunu ardışık düzen aracılığıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4724-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="f4724-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="f4724-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="f4724-119">Bu komut, kaynak KIMLIĞIYLE bir Azure SYNAPSE Analytics Spark havuzunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f4724-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="f4724-120">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="f4724-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="f4724-121">Bu komut, Azure SYNAPSE Analytics Spark havuzu için otomatik ölçeği olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="f4724-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f4724-122">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="f4724-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="f4724-123">Bu komut, Azure SYNAPSE Analytics Spark havuzu için otomatik ölçeği devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f4724-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f4724-124">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="f4724-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="f4724-125">Bu komut bir Azure SYNAPSE Analytics Spark havuzu için otomatik duraklatma 'yi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="f4724-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="f4724-126">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="f4724-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="f4724-127">Bu komut, Azure SYNAPSE Analytics Spark havuzu için otomatik duraklatma özelliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="f4724-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f4724-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4724-128">PARAMETERS</span></span>

### <span data-ttu-id="f4724-129">-Iş</span><span class="sxs-lookup"><span data-stu-id="f4724-129">-AsJob</span></span>
<span data-ttu-id="f4724-130">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f4724-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4724-131">-Autopausedelayınminute</span><span class="sxs-lookup"><span data-stu-id="f4724-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="f4724-132">Dakika sayısı.</span><span class="sxs-lookup"><span data-stu-id="f4724-132">Number of minutes idle.</span></span> <span data-ttu-id="f4724-133">Otomatik duraklatma etkinleştirildiğinde bu parametrenin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f4724-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="f4724-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="f4724-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="f4724-135">Belirtilen Spark havuzunda ayrılacak en fazla düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="f4724-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="f4724-136">Otomatik ölçek etkinleştirildiğinde bu parametrenin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f4724-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="f4724-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="f4724-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="f4724-138">Belirtilen Spark havuzunda ayrılacak en az düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="f4724-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="f4724-139">Otomatik ölçek etkinleştirildiğinde bu parametrenin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f4724-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="f4724-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4724-140">-DefaultProfile</span></span>
<span data-ttu-id="f4724-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4724-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4724-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="f4724-142">-EnableAutoPause</span></span>
<span data-ttu-id="f4724-143">Otomatik duraklatma özelliğinin etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4724-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-144">-Enableotomatik ölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="f4724-144">-EnableAutoScale</span></span>
<span data-ttu-id="f4724-145">Otomatik ölçeğin etkinleştirilip etkinleştirilmeyeceğini gösterir</span><span class="sxs-lookup"><span data-stu-id="f4724-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4724-146">-InputObject</span></span>
<span data-ttu-id="f4724-147">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f4724-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-148">-Librarygereksinimlerdosyayolu</span><span class="sxs-lookup"><span data-stu-id="f4724-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="f4724-149">Ortam yapılandırma dosyası ("zar dondurma" çıktısı).</span><span class="sxs-lookup"><span data-stu-id="f4724-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="f4724-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4724-150">-Name</span></span>
<span data-ttu-id="f4724-151">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="f4724-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f4724-152">-NodeCount</span></span>
<span data-ttu-id="f4724-153">Belirtilen Spark havuzunda tahsis edilecek düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="f4724-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="f4724-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="f4724-154">-NodeSize</span></span>
<span data-ttu-id="f4724-155">Belirtilen Spark havuzunda tahsis edilen düğümlerde kullanılacak çekirdek ve bellek sayısı.</span><span class="sxs-lookup"><span data-stu-id="f4724-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="f4724-156">Otomatik ölçek devre dışı bırakıldığında bu parametre belirtilmelidir</span><span class="sxs-lookup"><span data-stu-id="f4724-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4724-157">-ResourceGroupName</span></span>
<span data-ttu-id="f4724-158">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f4724-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-159">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f4724-159">-ResourceId</span></span>
<span data-ttu-id="f4724-160">SYNAPSE Spark havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f4724-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-161">-Parlak sürüm</span><span class="sxs-lookup"><span data-stu-id="f4724-161">-SparkVersion</span></span>
<span data-ttu-id="f4724-162">Apache Spark sürümü.</span><span class="sxs-lookup"><span data-stu-id="f4724-162">Apache Spark version.</span></span>
<span data-ttu-id="f4724-163">İzin verilen değerler: 2,4</span><span class="sxs-lookup"><span data-stu-id="f4724-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="f4724-164">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f4724-164">-Tag</span></span>
<span data-ttu-id="f4724-165">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="f4724-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="f4724-166">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="f4724-166">-WorkspaceName</span></span>
<span data-ttu-id="f4724-167">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="f4724-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-168">-</span><span class="sxs-lookup"><span data-stu-id="f4724-168">-WorkspaceObject</span></span>
<span data-ttu-id="f4724-169">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="f4724-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4724-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4724-170">-Confirm</span></span>
<span data-ttu-id="f4724-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4724-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4724-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4724-172">-WhatIf</span></span>
<span data-ttu-id="f4724-173">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4724-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4724-174">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4724-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4724-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4724-175">CommonParameters</span></span>
<span data-ttu-id="f4724-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4724-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4724-177">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4724-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4724-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4724-178">INPUTS</span></span>

### <span data-ttu-id="f4724-179">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f4724-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f4724-180">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f4724-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f4724-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4724-181">OUTPUTS</span></span>

### <span data-ttu-id="f4724-182">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f4724-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f4724-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4724-183">NOTES</span></span>

## <span data-ttu-id="f4724-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4724-184">RELATED LINKS</span></span>
