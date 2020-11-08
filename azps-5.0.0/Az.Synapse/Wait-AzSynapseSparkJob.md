---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277130"
---
# <span data-ttu-id="481b4-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="481b4-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="481b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="481b4-102">SYNOPSIS</span></span>
<span data-ttu-id="481b4-103">SYNAPSE Analizi Spark işinin tamamlamasını bekler.</span><span class="sxs-lookup"><span data-stu-id="481b4-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="481b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="481b4-104">SYNTAX</span></span>

### <span data-ttu-id="481b4-105">Waitparlak Jobbyidparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="481b4-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="481b4-106">Waitparlak Jobbyıdfromparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="481b4-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="481b4-107">Waitminijobbyıdfrominputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="481b4-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="481b4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="481b4-108">DESCRIPTION</span></span>
<span data-ttu-id="481b4-109">**Wait-AzSynapseSparkJob** cmdlet 'ı bir Azure SYNAPSE Analytics işinin tamamlamasını bekler.</span><span class="sxs-lookup"><span data-stu-id="481b4-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="481b4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="481b4-110">EXAMPLES</span></span>

### <span data-ttu-id="481b4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="481b4-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="481b4-112">Bu komut belirtilen KIMLIğIN tamamlanma işine yönelik bekler.</span><span class="sxs-lookup"><span data-stu-id="481b4-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="481b4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="481b4-113">PARAMETERS</span></span>

### <span data-ttu-id="481b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481b4-114">-DefaultProfile</span></span>
<span data-ttu-id="481b4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="481b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="481b4-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="481b4-116">-LivyId</span></span>
<span data-ttu-id="481b4-117">Spark işinin tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="481b4-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481b4-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="481b4-118">-SparkJobObject</span></span>
<span data-ttu-id="481b4-119">Spark iş girişi nesnesi genellikle ardışık düzen aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="481b4-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="481b4-120">-Parlak PoolName</span><span class="sxs-lookup"><span data-stu-id="481b4-120">-SparkPoolName</span></span>
<span data-ttu-id="481b4-121">SYNAPSE Spark havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="481b4-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481b4-122">-Parlak Poolobject</span><span class="sxs-lookup"><span data-stu-id="481b4-122">-SparkPoolObject</span></span>
<span data-ttu-id="481b4-123">Genellikle ardışık düzen aracılığıyla geçen Spark havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="481b4-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="481b4-124">-Timeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="481b4-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="481b4-125">Hata vermeden önce beklenecek en uzun süre. Varsayılan değer asla zaman aşımına uğramayacak.</span><span class="sxs-lookup"><span data-stu-id="481b4-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="481b4-126">-Waitıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="481b4-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="481b4-127">Saniye cinsinden iş durumu denetimleri arasındaki yoklama aralığı.</span><span class="sxs-lookup"><span data-stu-id="481b4-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="481b4-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="481b4-128">-WorkspaceName</span></span>
<span data-ttu-id="481b4-129">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="481b4-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481b4-130">CommonParameters</span></span>
<span data-ttu-id="481b4-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="481b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481b4-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="481b4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481b4-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="481b4-133">INPUTS</span></span>

### <span data-ttu-id="481b4-134">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="481b4-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="481b4-135">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="481b4-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="481b4-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="481b4-136">OUTPUTS</span></span>

### <span data-ttu-id="481b4-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="481b4-137">System.Boolean</span></span>

## <span data-ttu-id="481b4-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="481b4-138">NOTES</span></span>

## <span data-ttu-id="481b4-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="481b4-139">RELATED LINKS</span></span>
