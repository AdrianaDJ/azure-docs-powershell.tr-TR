---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275364"
---
# <span data-ttu-id="62dee-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="62dee-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="62dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62dee-102">SYNOPSIS</span></span>
<span data-ttu-id="62dee-103">Bir Azure HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını açıklayan kalıcı olmayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62dee-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="62dee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62dee-104">SYNTAX</span></span>

### <span data-ttu-id="62dee-105">LoadAutoscaleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62dee-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62dee-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dee-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62dee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="62dee-107">DESCRIPTION</span></span>
<span data-ttu-id="62dee-108">**New-AzHDInsightClusterAutoscaleConfiguration** cmdlet 'ı bir Azure HDInsight kümesinin otomatik ölçeklendirme yapılandırmasını açıklayan kalıcı olmayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62dee-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="62dee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62dee-109">EXAMPLES</span></span>

### <span data-ttu-id="62dee-110">Örnek 1: yükleme tabanlı otomatik ölçeklendirme yapılandırmasını açıklayan bir nesne oluşturma</span><span class="sxs-lookup"><span data-stu-id="62dee-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="62dee-111">Bu komut, yükleme tabanlı otomatik ölçeklendirme yapılandırmasını tanımlayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62dee-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="62dee-112">Örnek 2: zamanlama tabanlı otomatik ölçeklendirme yapılandırmasını açıklayan bir nesne oluşturma</span><span class="sxs-lookup"><span data-stu-id="62dee-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="62dee-113">Bu komut, zamanlama tabanlı otomatik ölçeklendirme yapılandırmasını açıklayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62dee-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="62dee-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62dee-114">PARAMETERS</span></span>

### <span data-ttu-id="62dee-115">-Koşul</span><span class="sxs-lookup"><span data-stu-id="62dee-115">-Condition</span></span>
<span data-ttu-id="62dee-116">Zamanlamaya dayalı otomatik ölçeklendirme koşulunu alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62dee-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62dee-117">-DefaultProfile</span></span>
<span data-ttu-id="62dee-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62dee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62dee-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="62dee-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="62dee-120">Yükleme tabanlı otomatik ölçeklendirme 'nin maxhayvan workernode sayısını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62dee-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dee-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="62dee-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="62dee-122">Yükleme tabanlı otomatik ölçeklendirme 'nin en az workernode sayısını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62dee-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dee-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="62dee-123">-TimeZone</span></span>
<span data-ttu-id="62dee-124">Zamanlamaya dayalı otomatik ölçeklendirme saat dilimini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62dee-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62dee-125">CommonParameters</span></span>
<span data-ttu-id="62dee-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62dee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62dee-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62dee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62dee-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62dee-128">INPUTS</span></span>

### <span data-ttu-id="62dee-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62dee-129">None</span></span>

## <span data-ttu-id="62dee-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62dee-130">OUTPUTS</span></span>

### <span data-ttu-id="62dee-131">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="62dee-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="62dee-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62dee-132">NOTES</span></span>

## <span data-ttu-id="62dee-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62dee-133">RELATED LINKS</span></span>

<span data-ttu-id="62dee-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="62dee-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
