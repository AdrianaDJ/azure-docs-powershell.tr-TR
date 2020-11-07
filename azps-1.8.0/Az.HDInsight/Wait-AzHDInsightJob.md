---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: b603be88ffa89f730cfaaa2f67738cdadc2d4d25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916523"
---
# <span data-ttu-id="c0516-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c0516-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="c0516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0516-102">SYNOPSIS</span></span>
<span data-ttu-id="c0516-103">Belirtilen işin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="c0516-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="c0516-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0516-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0516-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0516-105">DESCRIPTION</span></span>
<span data-ttu-id="c0516-106">**Wait-AzHDInsightJob** cmdlet 'i, bir Azure HDInsight işinin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="c0516-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="c0516-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0516-107">EXAMPLES</span></span>

### <span data-ttu-id="c0516-108">Örnek 1: işin tamamlanmasını veya başarısızlığını bekleme</span><span class="sxs-lookup"><span data-stu-id="c0516-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="c0516-109">Bu komut, bir işin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="c0516-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="c0516-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0516-110">PARAMETERS</span></span>

### <span data-ttu-id="c0516-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0516-111">-ClusterName</span></span>
<span data-ttu-id="c0516-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0516-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0516-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0516-113">-DefaultProfile</span></span>
<span data-ttu-id="c0516-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c0516-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0516-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c0516-115">-HttpCredential</span></span>
<span data-ttu-id="c0516-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0516-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0516-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c0516-117">-JobId</span></span>
<span data-ttu-id="c0516-118">İşin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0516-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0516-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0516-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0516-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0516-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c0516-121">-Timeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="c0516-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="c0516-122">Saniye cinsinden iş tamamlanması için beklenecek toplam süre.</span><span class="sxs-lookup"><span data-stu-id="c0516-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="c0516-123">-Waitıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="c0516-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="c0516-124">Saniye cinsinden iş durumu denetimleri arasında bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="c0516-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="c0516-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0516-125">CommonParameters</span></span>
<span data-ttu-id="c0516-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0516-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0516-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0516-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0516-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0516-128">INPUTS</span></span>

### <span data-ttu-id="c0516-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c0516-129">System.String</span></span>

## <span data-ttu-id="c0516-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0516-130">OUTPUTS</span></span>

### <span data-ttu-id="c0516-131">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c0516-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="c0516-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0516-132">NOTES</span></span>

## <span data-ttu-id="c0516-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0516-133">RELATED LINKS</span></span>

[<span data-ttu-id="c0516-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c0516-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="c0516-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c0516-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="c0516-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c0516-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


