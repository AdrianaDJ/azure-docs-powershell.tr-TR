---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276316"
---
# <span data-ttu-id="36637-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="36637-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="36637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36637-102">SYNOPSIS</span></span>
<span data-ttu-id="36637-103">SYNAPSE çözümleme Spark havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36637-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="36637-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36637-104">SYNTAX</span></span>

### <span data-ttu-id="36637-105">Createbynaik Denableautoscaleparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36637-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36637-106">Createbynaik Vseçdisableautoscaleparameterset</span><span class="sxs-lookup"><span data-stu-id="36637-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36637-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="36637-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36637-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="36637-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36637-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="36637-109">DESCRIPTION</span></span>
<span data-ttu-id="36637-110">**New-AzSynapseSparkPool** cmdlet 'ı bir Azure SYNAPSE Analytics Spark havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36637-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="36637-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36637-111">EXAMPLES</span></span>

### <span data-ttu-id="36637-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36637-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="36637-113">Bu komut, bir Azure SYNAPSE Analytics Spark havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36637-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="36637-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="36637-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="36637-115">Bu komut, otomatik ölçeklendirme etkinleştirilmiş bir Azure SYNAPSE Analytics Spark havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36637-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="36637-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="36637-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="36637-117">Bu komut, ardışık düzen aracılığıyla bir Azure SYNAPSE Analytics Spark havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36637-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="36637-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="36637-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="36637-119">Bu komut, ardışık düzen aracılığıyla otomatik ölçek etkinleştirilmiş bir Azure SYNAPSE Analytics Spark havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36637-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="36637-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36637-120">PARAMETERS</span></span>

### <span data-ttu-id="36637-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="36637-121">-AsJob</span></span>
<span data-ttu-id="36637-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="36637-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36637-123">-Autopausedelayınminute</span><span class="sxs-lookup"><span data-stu-id="36637-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="36637-124">Dakika sayısı.</span><span class="sxs-lookup"><span data-stu-id="36637-124">Number of minutes idle.</span></span> <span data-ttu-id="36637-125">Otomatik duraklatma etkinleştirildiğinde bu parametrenin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="36637-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="36637-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="36637-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="36637-127">Belirtilen Spark havuzunda ayrılacak en fazla düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="36637-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="36637-128">Otomatik ölçek etkinleştirildiğinde bu parametrenin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="36637-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="36637-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="36637-130">Belirtilen Spark havuzunda ayrılacak en az düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="36637-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="36637-131">Otomatik ölçek etkinleştirildiğinde bu parametrenin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="36637-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36637-132">-DefaultProfile</span></span>
<span data-ttu-id="36637-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36637-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36637-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="36637-134">-EnableAutoPause</span></span>
<span data-ttu-id="36637-135">Otomatik duraklatma özelliğinin etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="36637-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="36637-136">-Librarygereksinimlerdosyayolu</span><span class="sxs-lookup"><span data-stu-id="36637-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="36637-137">Ortam yapılandırma dosyası ("zar dondurma" çıktısı).</span><span class="sxs-lookup"><span data-stu-id="36637-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="36637-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="36637-138">-Name</span></span>
<span data-ttu-id="36637-139">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="36637-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="36637-140">-NodeCount</span></span>
<span data-ttu-id="36637-141">Belirtilen Spark havuzunda tahsis edilecek düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="36637-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="36637-142">-NodeSize</span></span>
<span data-ttu-id="36637-143">Belirtilen Spark havuzunda tahsis edilen düğümlerde kullanılacak çekirdek ve bellek sayısı.</span><span class="sxs-lookup"><span data-stu-id="36637-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="36637-144">Otomatik ölçek devre dışı bırakıldığında bu parametre belirtilmelidir</span><span class="sxs-lookup"><span data-stu-id="36637-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36637-145">-ResourceGroupName</span></span>
<span data-ttu-id="36637-146">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="36637-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-147">-Parlak sürüm</span><span class="sxs-lookup"><span data-stu-id="36637-147">-SparkVersion</span></span>
<span data-ttu-id="36637-148">Apache Spark sürümü.</span><span class="sxs-lookup"><span data-stu-id="36637-148">Apache Spark version.</span></span>
<span data-ttu-id="36637-149">İzin verilen değerler: 2,4</span><span class="sxs-lookup"><span data-stu-id="36637-149">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="36637-150">-Tag</span></span>
<span data-ttu-id="36637-151">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="36637-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="36637-152">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="36637-152">-WorkspaceName</span></span>
<span data-ttu-id="36637-153">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="36637-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36637-154">-</span><span class="sxs-lookup"><span data-stu-id="36637-154">-WorkspaceObject</span></span>
<span data-ttu-id="36637-155">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="36637-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36637-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="36637-156">-Confirm</span></span>
<span data-ttu-id="36637-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36637-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36637-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36637-158">-WhatIf</span></span>
<span data-ttu-id="36637-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36637-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36637-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36637-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36637-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36637-161">CommonParameters</span></span>
<span data-ttu-id="36637-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36637-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36637-163">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36637-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36637-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36637-164">INPUTS</span></span>

### <span data-ttu-id="36637-165">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="36637-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="36637-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36637-166">OUTPUTS</span></span>

### <span data-ttu-id="36637-167">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="36637-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="36637-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36637-168">NOTES</span></span>

## <span data-ttu-id="36637-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36637-169">RELATED LINKS</span></span>
