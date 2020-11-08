---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109057"
---
# <span data-ttu-id="e9d1e-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e9d1e-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="e9d1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d1e-103">Belirtilen işin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="e9d1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9d1e-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d1e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d1e-106">**Wait-AzHDInsightJob** cmdlet 'i, bir Azure HDInsight işinin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="e9d1e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="e9d1e-108">Örnek 1: işin tamamlanmasını veya başarısızlığını bekleme</span><span class="sxs-lookup"><span data-stu-id="e9d1e-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="e9d1e-109">Bu komut, bir işin tamamlanmasını veya başarısızlığını bekler.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="e9d1e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9d1e-110">PARAMETERS</span></span>

### <span data-ttu-id="e9d1e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e9d1e-111">-ClusterName</span></span>
<span data-ttu-id="e9d1e-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e9d1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d1e-113">-DefaultProfile</span></span>
<span data-ttu-id="e9d1e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9d1e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9d1e-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e9d1e-115">-HttpCredential</span></span>
<span data-ttu-id="e9d1e-116">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="e9d1e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="e9d1e-117">-JobId</span></span>
<span data-ttu-id="e9d1e-118">İşin iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="e9d1e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9d1e-119">-ResourceGroupName</span></span>
<span data-ttu-id="e9d1e-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e9d1e-121">-Timeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="e9d1e-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="e9d1e-122">Saniye cinsinden iş tamamlanması için beklenecek toplam süre.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="e9d1e-123">-Waitıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="e9d1e-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="e9d1e-124">Saniye cinsinden iş durumu denetimleri arasında bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="e9d1e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d1e-125">CommonParameters</span></span>
<span data-ttu-id="e9d1e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9d1e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d1e-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d1e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d1e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9d1e-128">INPUTS</span></span>

### <span data-ttu-id="e9d1e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e9d1e-129">System.String</span></span>

## <span data-ttu-id="e9d1e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9d1e-130">OUTPUTS</span></span>

### <span data-ttu-id="e9d1e-131">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e9d1e-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="e9d1e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9d1e-132">NOTES</span></span>

## <span data-ttu-id="e9d1e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9d1e-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9d1e-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e9d1e-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="e9d1e-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e9d1e-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="e9d1e-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e9d1e-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


