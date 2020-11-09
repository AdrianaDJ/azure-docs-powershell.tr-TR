---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319558"
---
# <span data-ttu-id="e291b-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e291b-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="e291b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e291b-102">SYNOPSIS</span></span>
<span data-ttu-id="e291b-103">Azure HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e291b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e291b-104">SYNTAX</span></span>

### <span data-ttu-id="e291b-105">LoadAutoscaleByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e291b-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e291b-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e291b-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e291b-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e291b-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e291b-108">Loadautoscalebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e291b-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e291b-109">Scheduleautoscalebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e291b-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e291b-110">Autoscaleconfigurationbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e291b-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e291b-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e291b-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e291b-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e291b-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e291b-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e291b-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e291b-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="e291b-114">DESCRIPTION</span></span>
<span data-ttu-id="e291b-115">Bu cmdlet **kümesi-AzHDInsightClusterAutoscaleConfiguration** , Azure HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e291b-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e291b-116">EXAMPLES</span></span>

### <span data-ttu-id="e291b-117">Örnek 1: HDInsight kümesinin yük tabanlı yükleme otomatik ölçeklendirme yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e291b-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="e291b-118">Bu komut, Azure HDInsight kümesinin yük tabanlı otomatik ölçeklendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="e291b-119">Örnek 2: HDInsight kümesinin zamanlama tabanlı otomatik ölçeklendirme boyutunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="e291b-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="e291b-120">Bu komut HDInsight kümesinin zamanlama tabanlı otomatik ölçeklendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="e291b-121">Örnek 3: otomatik ölçeklendirme yapılandırmasını ayarlamış başka bir kümeyi temel alan HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e291b-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="e291b-122">Bu komut, HDInsight kümesinin başka bir kümeyi temel alan otomatik ölçeklendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="e291b-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e291b-123">PARAMETERS</span></span>

### <span data-ttu-id="e291b-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="e291b-124">-AsJob</span></span>
<span data-ttu-id="e291b-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e291b-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e291b-126">-Otomatik ölçek yapılandırması</span><span class="sxs-lookup"><span data-stu-id="e291b-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="e291b-127">Otomatik ölçeklendirme yapılandırmasını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="e291b-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e291b-128">-ClusterName</span></span>
<span data-ttu-id="e291b-129">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-130">-Koşul</span><span class="sxs-lookup"><span data-stu-id="e291b-130">-Condition</span></span>
<span data-ttu-id="e291b-131">Zamanlamaya dayalı otomatik ölçeklendirme koşulunu alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e291b-132">-DefaultProfile</span></span>
<span data-ttu-id="e291b-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e291b-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e291b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e291b-134">-InputObject</span></span>
<span data-ttu-id="e291b-135">Giriş nesnesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="e291b-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="e291b-137">Yükleme tabanlı otomatik ölçeklendirme 'nin maxhayvan workernode sayısını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="e291b-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="e291b-139">Yükleme tabanlı otomatik ölçeklendirme 'nin en az workernode sayısını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e291b-140">-ResourceGroupName</span></span>
<span data-ttu-id="e291b-141">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e291b-142">-ResourceId</span></span>
<span data-ttu-id="e291b-143">Kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-144">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="e291b-144">-Schedule</span></span>
<span data-ttu-id="e291b-145">Zamanlamaya dayalı parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="e291b-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="e291b-146">-TimeZone</span></span>
<span data-ttu-id="e291b-147">Zamanlamaya dayalı otomatik ölçeklendirme saat dilimini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e291b-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e291b-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="e291b-148">-Confirm</span></span>
<span data-ttu-id="e291b-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e291b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e291b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e291b-150">-WhatIf</span></span>
<span data-ttu-id="e291b-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e291b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e291b-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e291b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e291b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e291b-153">CommonParameters</span></span>
<span data-ttu-id="e291b-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e291b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e291b-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e291b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e291b-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e291b-156">INPUTS</span></span>

### <span data-ttu-id="e291b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e291b-157">System.String</span></span>

### <span data-ttu-id="e291b-158">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e291b-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e291b-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e291b-159">OUTPUTS</span></span>

### <span data-ttu-id="e291b-160">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="e291b-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="e291b-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e291b-161">NOTES</span></span>

## <span data-ttu-id="e291b-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e291b-162">RELATED LINKS</span></span>

<span data-ttu-id="e291b-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e291b-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
