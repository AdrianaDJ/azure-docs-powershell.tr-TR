---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275363"
---
# <span data-ttu-id="2f77d-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="2f77d-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="2f77d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f77d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f77d-103">Zamanlamaya dayalı otomatik ölçeklendirme koşulu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f77d-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="2f77d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f77d-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f77d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f77d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f77d-106">**New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet 'i zamanlamaya dayalı otomatik ölçeklendirme koşulu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f77d-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="2f77d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f77d-107">EXAMPLES</span></span>

### <span data-ttu-id="2f77d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f77d-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="2f77d-109">Bu komut, 09:00 kümenin her Pazartesi, Çarşamba.</span><span class="sxs-lookup"><span data-stu-id="2f77d-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="2f77d-110">Örnek 2: otomatik ölçeklendirme koşuluna sahip bir kümenin zamanlamaya dayalı otomatik ölçeklendirme özelliğini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="2f77d-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="2f77d-111">Bu komut, 09:00 kümenin her Pazartesi, Çarşamba.</span><span class="sxs-lookup"><span data-stu-id="2f77d-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="2f77d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f77d-112">PARAMETERS</span></span>

### <span data-ttu-id="2f77d-113">-Günlük</span><span class="sxs-lookup"><span data-stu-id="2f77d-113">-Day</span></span>
<span data-ttu-id="2f77d-114">Otomatik ölçeklendirme zamanlama koşulunun günlerini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2f77d-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f77d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f77d-115">-DefaultProfile</span></span>
<span data-ttu-id="2f77d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f77d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f77d-117">Defalık</span><span class="sxs-lookup"><span data-stu-id="2f77d-117">-Time</span></span>
<span data-ttu-id="2f77d-118">Otomatik ölçeklendirme zamanlama koşulu süresini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2f77d-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f77d-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="2f77d-119">-WorkerNodeCount</span></span>
<span data-ttu-id="2f77d-120">Otomatik ölçeklendirme zamanlama koşulunun zamanlama workernode sayısını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2f77d-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f77d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f77d-121">CommonParameters</span></span>
<span data-ttu-id="2f77d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f77d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f77d-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2f77d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f77d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f77d-124">INPUTS</span></span>

### <span data-ttu-id="2f77d-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2f77d-125">None</span></span>

## <span data-ttu-id="2f77d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f77d-126">OUTPUTS</span></span>

### <span data-ttu-id="2f77d-127">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="2f77d-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="2f77d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f77d-128">NOTES</span></span>

## <span data-ttu-id="2f77d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f77d-129">RELATED LINKS</span></span>

<span data-ttu-id="2f77d-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f77d-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
